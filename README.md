# AI-image-madness
Exploration of AI image generqation

### Introductory material   
[The text-to-image revolution, explained](https://www.vox.com/23150422/text-to-image-ai-deep-learning)   
[Eliso’s Generative Art Guides](https://botbox.dev/)   
[Making AI Art With Midjourney](https://www.slaphappylarry.com/making-ai-art-with-midjourney/)   

### TEXT to IMAGE engines
[Dall-e2](https://openai.com/dall-e-2/) : paying servide on-line   
[Midjourney](https://www.midjourney.com/home/) : paying servide on-line   
[Disco Diffusion](https://botbox.dev/disco-diffusion-guide/), [here also](http://discodiffusion.com/): Free, local computer and slow    
[Night Cafe](https://creator.nightcafe.studio/text-to-image-art) : web based   
[Stable Diffusion](https://stability.ai/)   
GUI para "Stable Diffusion". Ejecutable en Windows que lo hace todo [NMKD Stable Diffusion](https://nmkd.itch.io/t2i-gui)   

### STABLE DIFFUSION   

**Seed //** is a number that controls the initial noise.    
**Step count //** this parameter controls the number of these denoising steps to final image   
**Diffusion samplers //** are the method used to denoise the image during generation. Use DDIM for beginners at 10 steps.   

**Textual Inversion //** Metodo de aprendizaje de nuevos modelos (Objetos, animales, personas,...) utilizando el modelo SD EXISTENTE. No lo modifica, solamente intenta generar un nuevo "token"  dentro del "latent space" que ya tiene. El resutando es un "embedding" de poco peso (4Mb) que se puede llamar utilizando el "token".

**Textual Inversions**, Text-to-Image pairs added on top of the Existing model and do not change the original,   
**Dreambooth**, Retrains a Existing Model and Integrates the Text-to-Image Pair into the model.   
**Hypernetworks**, Add New Weights to the calculations to Existing Text-to-Image Pairs on top of the Model, They do not change the Model   

How to and Tips:   
- [SD basic / intermediate guide on Reddit](https://www.reddit.com/r/StableDiffusion/comments/x41n87/how_to_get_images_that_dont_suck_a/)   
- [Stable Diffusion: Tutorials, Resources, and Tools](https://stackdiary.com/stable-diffusion-resources/)   
- [Styles of drawing / painting](https://docs.google.com/document/d/1ZtNwY1PragKITY0F4R-f8CarwHojc9Wrf37d0NONHDg/edit#heading=h.kn3gjdhgaoek) Con imagenes de guia, interesante para fijar un tipo de estilo a las imagenes.
- [How to draw and paint with SD. Compositing images](https://andys.page/posts/how-to-draw/#) Muy interesante para aprender a dirigir SD y mezclar elementos   
- [SD prompting cheatsheet](https://moritz.pm/posts/parameters)
- [ Akashic Records / A compendium of information regarding Stable Diffusion (SD)](https://github.com/Maks-s/sd-akashic) *Interesante*   
- Para quitar la "censura". [Remove SAFETY filter](https://www.reddit.com/r/StableDiffusion/comments/wv2nw0/tutorial_how_to_remove_the_safety_filter_in_5/)   

PROMPT Craft
- [Help with facial descriptions (for writers)](https://www.bryndonovan.com/2015/06/16/master-list-of-physical-descriptions/)   
- [Lexica: images and prompts](https://lexica.art/)   
- [A.I Text promp generator (with images)](https://aitextpromptgenerator.com/)

GUI and installers   
- [NMKD Stable Diffusion GUI // Instalación totalmente automatica](https://nmkd.itch.io/t2i-gui)   
- [Stable Diffusion web UI (AUTOMATIC1111)](https://github.com/AUTOMATIC1111/stable-diffusion-webui) and [Interesting documentation](https://hub.tcno.co/ai/stable-diffusion/webui/)    
    - To update repo, CMD/Bash and go to distribution and `git pull` to get last version from GitHub   
    - Intall Krita fork [from 1111](https://github.com/Interpause/auto-sd-krita/wiki/Install-Guide#plugin-installation)   
    - [Quick switch from Krita to 1111 fork](https://github.com/Interpause/auto-sd-krita/wiki/Quick-Switch-Using-Existing-AUTOMATIC1111-Install)   
- [AI Image Generator GUI | aiimag.es](https://sunija.itch.io/aiimages)    
- [KRITA SD Plug-in](https://www.flyingdog.de/sd/en/)   
- [KOI Krita Open (source) img2img](https://github.com/nousr/koi)   

Models    
- [Stable Diffusion Models](https://rentry.org/sdmodels)    
- [Modern Disney](https://huggingface.co/nitrosocke/mo-di-diffusion)    
- [Classic Animation](https://huggingface.co/nitrosocke/classic-anim-diffusion)    
- [Tron Legacy](https://huggingface.co/dallinmackay/Tron-Legacy-diffusion)    
- [Waifu diffusion(1.3) - Anime look](https://huggingface.co/hakurei/waifu-diffusion-v1-3)   

Textual inversion (learn new models for SD):
- [Textual Inversion - Make Anything In Stable Diffusion!](https://www.youtube.com/watch?v=7Lxdk89W2K0&t=91s)    
- [TEXTUAL INVERSION - How To Do It In Stable Diffusion(AUTOMATIC1111)](https://www.youtube.com/watch?v=MLz0iM0M7Fk)    

Dreambooth (learning new models to use with SD)   
- [Dreambooth on Stable Diffusion](https://github.com/gammagec/Dreambooth-SD-optimized)   
- [ DreamBooth on SD on a 3090](https://www.reddit.com/r/StableDiffusion/comments/xo4onu/using_dreambooth_on_sd_on_a_3090_w24gb_vram_about/)   
- [Dreambooth on Windows via Linux virtual enviroment](https://www.youtube.com/watch?v=w6PTviOCYQY&t=0s)   

- [Automatic1111 Guide to train youre face (Hypernetwork)](https://www.youtube.com/watch?v=P1dfwViVOIU)   

SD Samplers (resumen subjetivo)   
Los samplers suelen modificar significativamente la imagen con los valores de "steps" bajos. De 10 a 50 suele haber cambio.    
- Euler : Bastante estable. Inutil pasar de 30 "steps", no cambia.   
- Euler a (adaptativo): Sampler cambia notablemente al subir "steps". Util de 10 a 100.   
- Heun : Resultados parecidos a "Euler". Es estable y como maximo 30 "steps"   
- LMS : (rango haste 50) ESTE ES EL QUE VIENE POR DEFECTO   
- PLMS : (rango  10-60)
- DDIM  : (rango  10-60)   
- DPM : (rango hasta 10). Este sampler da imagenes muy diferentes de los otros.   
- DPM Fast : (rango 10-150). Muy inestable, cambia mucho lo que vemos con diferentes "steps". <Muy diferente el resultado de otros samplers. A partir de 90 "steps" parece que no cambia tanto.   
- DPM 2 : (rango hasta 40) parecido a la "norma"   
- DPM 2 Adaptive : (rango hasta 100) Muy variable al principio (primeros "steps"), luego se vuelve mas estable.   
- DPM 2 A Karras : (rango hasta 100) Variable al principo, luego converge mas o menos como los otros.   
- DPM 2 Karras : (rango hasta 30) cambia el resultados respecto a los otros.   

Estilos para Stable Diffusion   
[artists whose names can be added to Stable Diffusion prompts](https://github.com/kaikalii/stable-diffusion-artists)   

### SCALE IMAGES with AI   
Estas herramientas suelen ir incluidas en las GUI de los "engines"   

[Real ERSGAN](https://github.com/xinntao/Real-ESRGAN)   
[ERSGAN with GUI](https://github.com/n00mkrad/cupscale)   
