IN/OUT PAinting:


1) Escalar imagen en photoshop / Krita / Gimp / Whatever (canvas, incorporando lo que queremos ampliar)
2) Pintar el trozo ampliado con colores (pueden ser solidos) que reflejen lo que queremos que haya (cielo, suelo, edificios, etc.)
3) Seleccionar  sd-v1.5-inpainting.ckpt (el especial para "inpaint")
4) Incorporar imagen seleccionada en img2img
5) Enmascarar en SD-web-UI las partes pintadas (por partes si estan separadas)
6) Opciones 
    - Masked content --> Original : Lo que fabrique nuevo estara basado en lo ya existente.
    - Inpint at full resolution : 
    - Crop and resize
    - Sampling steps : unos 30 // Sampling method : DPM fast
    - Width / Height al tamanyo que queramos que la nueva parte se fabrique. Luego la escala y la pega en la imagen final
    - Denoise strength --> 0.85 : Tipicamete alto para que modifique la imagen mas. 0 es nada, 1 es me lo invento todo.
7) Prompt: parecido al del estilo que ya existe en la imagen, pero con las incorporaciones o modificaciones de lo que queramos que salga.
8) Utilizar el mismo "seed" para que se parezca, al menos al principio.
