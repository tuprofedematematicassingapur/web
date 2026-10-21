# Versión B · landing para padres

Página de inicio única (método, seminarios y precios, cómo es un seminario online, cursos, sobre mí, dudas, contacto) + blog. Las URLs antiguas redirigen a su sección.

**Foto:** guarda tu foto como `assets/jose.jpg` y en `index.html` busca el comentario `FOTO:` y sustituye el bloque de la "J" por la línea indicada.

---

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub (por ejemplo `tuprofedematematicassingapur`). Puede ser público.
2. Sube **el contenido** de esta carpeta (no la carpeta en sí) a la raíz del repositorio. Asegúrate de que se suben también `CNAME` y `.nojekyll` (son archivos ocultos en algunos sistemas).
3. En el repositorio: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, rama `main`, carpeta `/ (root)`.
4. En **Settings → Pages → Custom domain** debe aparecer `tuprofedematematicassingapur.com` (lo lee del archivo `CNAME`).
5. Cuando el DNS esté cambiado (paso siguiente) y GitHub lo valide, marca **Enforce HTTPS**.

## Cambiar el DNS en IONOS

En IONOS → Dominios → tu dominio → DNS:

1. **Borra** los registros A / AAAA que apuntan al hosting de IONOS para `@` y el CNAME o A de `www`.
2. Añade estos 4 registros **A** para `@`:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
3. (Opcional, IPv6) 4 registros **AAAA** para `@`:
   - 2606:50c0:8000::153
   - 2606:50c0:8001::153
   - 2606:50c0:8002::153
   - 2606:50c0:8003::153
4. Un registro **CNAME** para `www` → `TU_USUARIO.github.io`
5. **No toques los registros MX** si tu email `info@tuprofedematematicassingapur.com` está en IONOS: el correo debe seguir funcionando.

La propagación puede tardar desde minutos hasta 24-48 h. Comprueba estas IPs en la documentación oficial de GitHub antes de aplicarlas: https://docs.github.com/es/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Antes de dar de baja el hosting de IONOS

- Verifica que la nueva web carga en tu dominio con HTTPS.
- Si quieres conservar algo del WordPress (imágenes, comentarios, copia de seguridad), descárgalo antes.
- Comprueba que **el correo** no depende del paquete de hosting que vas a cancelar.
