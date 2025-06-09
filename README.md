<h1>Automatic1111 Stable Diffusion web UI 4 runpod</h1>

[![RunPod](https://api.runpod.io/badge/runpod-workers/worker-a1111)](https://www.runpod.io/console/hub/runpod-workers/worker-a1111)

- Runs [Automatic1111 Stable Diffusion WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) and exposes its `txt2img` API endpoint
- Comes pre-packaged with the [**Deliberate v6**](https://huggingface.co/XpucT/Deliberate) model and [**CasiAI + Lalufem**](https://sd.h9k.wtf/models/CasioAi_LAlufem)

---

## Usage

The `input` object accepts any valid parameter for the Automatic1111 `/sdapi/v1/txt2img` endpoint. Refer to the [Automatic1111 API Documentation](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/API) for a full list of available parameters (like `seed`, `sampler_name`, `batch_size`, `styles`, `override_settings`, etc.).

### Example Request

Here's an example payload to generate an image:

```json
{
  "input": {
    "prompt": "Lalufem portrait face (age 27:1.4) and blue hair sitting crossed leg on a brown bed, wearing black lingerie, watching down to the blunt she is building. the wall in background ist light brown. Studio fot taken by flash with softbox, by Annie Leibovitz, 80mm, hasselblad, ultra realistic. with dancing shawdows. (looking to cam:1.2) (smiling:1.4)",
    "negative_prompt": "text, watermark, blurry, low quality, (worst quality, low quality, normal quality:2), lowres, blurry, jpeg artifacts, watermark, signature, text, error, cropped, out of frame, bad anatomy, extra limbs, missing limbs, mutated hands, bad hands, fused fingers, too many fingers, long neck, distorted face, cross-eye, lazy eye, bad eyes, bad proportions, cloned face, ugly face, poorly drawn face, malformed limbs, mutated body, disfigured, deformed, extra arms, extra legs, fat, overweight, unrealistic body, unnatural body, poorly drawn, (bad art), (bad lighting), (bad shadows), low detail, bad composition, wrong perspective, noisy image, grain, duplicate, out of focus, dirty, messy, glitched, overexposed, underexposed, bad outfit, wrong clothes, unrealistic clothing, missing clothing, censored, offensive, disturbing, ugly, (disfigured face:1.5), (worst face), unnatural colors, overly saturated, poorly rendered, unrealistic, wrong style, morbid, mutilated, child, childish",
    "steps": 25,
    "cfg_scale": 7,
    "width": 512,
    "height": 768,
    "sampler_name": "DPM++ 2M Karras"
  }
}
```
