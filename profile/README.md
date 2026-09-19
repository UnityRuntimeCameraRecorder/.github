# Runtime Camera Recorder for Unity

So, what's it all about?

Picture this: you're playing your favorite game and think, “Hey, it'd be pretty cool to record my finest moments—but without the UI getting in the way.”

And while we're at it, why settle for one video? Why not record several at once, each from a different point of view?

That’s the whole idea behind **Runtime Camera Recorder for Unity**.

Give it one, two, or maybe three cameras, and it'll record their footage as efficiently as possible—without slowing down the runtime—the game.

# Current Support

| OS | GPU | Graphics API | Status |
| --- | --- | --- | --- |
| Windows x64 | NVIDIA GPU with NVENC | Direct3D 11 | ✅ Supported |
| Windows x64 | AMD | Direct3D 11 | 🔭 On the wishlist |
| Windows x64 | Intel | Direct3D 11 | 🔭 On the wishlist |
| Windows x64 | NVIDIA GPU with NVENC | Direct3D 12 | 🔭 On the wishlist |
| Linux | NVIDIA, AMD, or Intel | Vulkan | 🔭 On the wishlist |
| macOS | Apple silicon | Metal | 🔭 On the wishlist |

# Repositories

| Repository | Purpose |
| --- | --- |
| [UnityMediaRecorder](https://github.com/UnityRuntimeCameraRecorder/UnityMediaRecorder) | Records Unity cameras and screen output with audio. |
| [Direct3DVideoEncoder](https://github.com/UnityRuntimeCameraRecorder/Direct3DVideoEncoder) | Encodes Direct3D 11 textures using NVIDIA NVENC. |
| [FFmpegMediaWriter](https://github.com/UnityRuntimeCameraRecorder/FFmpegMediaWriter) | Combines encoded video and raw audio into MP4 files. |
| [UnitySample](https://github.com/UnityRuntimeCameraRecorder/UnitySample) | Demonstrates camera and screen recording in an editable Unity project. |

# UnitySample Architecture

```mermaid
flowchart TB

    subgraph Sample["UnitySample — 2 cameras recording example"]
        direction LR
        Camera1["Camera 1<br/>Scene view"]
        Camera2["Camera 2<br/>Alternate view"]
        Audio["Unity audio mix"]
    end

    Camera1 --> Recorder1["UnityMediaRecorder #1"]
    Camera2 --> Recorder2["UnityMediaRecorder #2"]

    Audio --> Recorder1
    Audio --> Recorder2

    Recorder1 --> Encoder1["Direct3DVideoEncoder"]
    Recorder2 --> Encoder2["Direct3DVideoEncoder"]

    Encoder1 --> Writer1["FFmpegMediaWriter"]
    Encoder2 --> Writer2["FFmpegMediaWriter"]

    Recorder1 -->|"PCM audio"| Writer1
    Recorder2 -->|"PCM audio"| Writer2

    Writer1 --> Output1["Camera 1.mp4"]
    Writer2 --> Output2["Camera 2.mp4"]

    classDef camera fill:#593d88,color:#fff,stroke:#b99ae8,stroke-width:2px;
    classDef library fill:#176b87,color:#fff,stroke:#64ccc5,stroke-width:2px;
    classDef audio fill:#2d4356,color:#fff,stroke:#a7c4bc,stroke-width:2px;
    classDef output fill:#1f8a70,color:#fff,stroke:#9de8d7,stroke-width:2px;
    class Camera1,Camera2 camera;
    class Recorder1,Recorder2,Encoder1,Encoder2,Writer1,Writer2 library;
    class Audio audio;
    class Output1,Output2 output;
```

# Contributing

Want to help move things off the wishlist? Contributions are more than welcome!

You can help by testing the recorder on your OS and GPU, then sharing your setup and performance results. Please include your OS, GPU model, Unity version, graphics API, and anything that worked—or didn't.

Feeling like writing some code? You can also help build support for the platforms, GPUs, and graphics APIs that aren't supported yet. Pick something from the wishlist, open an issue to discuss your approach, and let's make it happen.
