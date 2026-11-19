# 5objeccionesbasicas — dónde está todo

Entrenador de objeciones (web estática).

| Pieza | Dónde |
|---|---|
| Web pública | https://5objeccionesbasicas.peterestela.com |
| Archivos de la web | `public/` (index.html, video, PDF, música, portada) |
| Repo anterior | https://github.com/peterestelaweb/objeccionesbasicas (no se usa; se conserva) |
| Origen | `../ADAPTACIONES DE VIDEO - VIDEO LAB/casos/2026-11-18-objeciones-lifeplus/objeccionesbasicas-web.zip` |
| Repo GitHub | https://github.com/peterestelaweb/5objeccionesbasicas |
| Deploy | `.github/workflows/deploy.yml` → FTPS (FTP-Deploy-Action) al hacer push a `main` |
| Servidor | Bana Hosting `bh8918.banahosting.com`, document root `/home/sagrxtar/5objeccionesbasicas.peterestela.com` |
| FTP cautivo | `deploy@5objeccionesbasicas.peterestela.com`, home = document root, `FTP_SERVER_DIR=/` |

## Cómo actualizar

1. Cambiar archivos en `public/`.
2. `git commit` + `git push` a `main`.
3. Comprobar que `https://5objeccionesbasicas.peterestela.com/deploy-marker.txt` muestra el commit nuevo (el workflow lo verifica solo).

La contraseña FTP solo está en el secret `FTP_PASSWORD` de GitHub y en cPanel (la puso Peter el 19-11-2026). `~/.config/objeccionesbasicas/ftp-pass` ya NO coincide: para cambiarla, Peter pega el mismo valor en cPanel → Change Password y en `gh secret set FTP_PASSWORD -R peterestelaweb/5objeccionesbasicas`.

Publicada y verificada el 19-11-2026: run 44472009830, `deploy-marker.txt` con commit 84bfc57.
