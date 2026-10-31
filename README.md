# Video Frame Extractor

This Cog model extracts either the first or last frame from any video file and outputs it as a high-quality JPEG image.

## Model Description

Video Frame Extractor is a simple utility model that:
- Takes any supported video file format as input
- Extracts either the first or last frame (user selectable)
- Outputs the extracted frame as a high-quality JPEG image

## Input Parameters

- `video`: The input video file (required)
- `return_first_frame`: Toggle to extract the first frame instead of the last frame (default: false)

## Output

A single JPEG image containing the extracted frame from the video.

## Example Usage

### Extract Last Frame (Default)

```bash
cog predict -i video=@sample_video.mp4
```

### Extract First Frame

```bash
cog predict -i video=@sample_video.mp4 -i return_first_frame=true
```

## Use Cases

- Create thumbnails from videos
- Extract key frames for analysis
- Generate preview images from video content
- Simplify video-to-image conversion workflows

## Technical Information

This model uses OpenCV (cv2) to process video files and extract frames with high fidelity. It supports all video formats compatible with OpenCV. 

## License

The code in this repository is licensed under the [Apache License 2.0](LICENSE).
