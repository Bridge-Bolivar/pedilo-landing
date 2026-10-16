# pedilo-landing

Landing global de la marca **Pedilo** en `https://pedilo.net`: presenta la marca y lleva a
`delivery.pedilo.net` (Pedilo Delivery) y `market.pedilo.net` (Pedilo Market).

Es un sitio estático: `index.html`, `styles.css` y `assets/` al lado. Sin build, sin
dependencias. La spec está en `SPEC.md`.

## Ver en local

```
python3 -m http.server 8080
```

y abrir `http://localhost:8080`.

## Deploy

Vive en el VPS de Baehost (el mismo de Engram y de las apps), servido por el Caddy del host
desde `/opt/pedilo-landing`. Primera vez, en el VPS:

```
sudo git clone https://github.com/Bridge-Bolivar/pedilo-landing /opt/pedilo-landing
```

Bloque en `/etc/caddy/Caddyfile`:

```
pedilo.net {
    root * /opt/pedilo-landing
    file_server
    encode gzip
    header Cache-Control "public, max-age=3600"
}

www.pedilo.net {
    redir https://pedilo.net{uri} permanent
}
```

y `sudo systemctl reload caddy`. Caddy saca el certificado solo cuando el DNS apunta al VPS.

Cada cambio que entra a `main` se publica con:

```
cd /opt/pedilo-landing && sudo git pull
```

## DNS (Namecheap, Advanced DNS)

| Tipo | Host | Valor |
|---|---|---|
| A | `@` | `168.205.94.151` |
| CNAME | `www` | `pedilo.net` |

## Pendiente

- WhatsApp de contacto. El mail del pie es `hola@pedilo.net`.
