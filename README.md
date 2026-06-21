# Try-On Proxy

Kleiner Vermittler-Server zwischen der Try-On-App und Replicate.
Hält den API-Key versteckt, damit er nicht im Browser sichtbar ist.

## Einrichtung (einmalig)

1. Dieses Verzeichnis als neues Repository auf GitHub hochladen
   (z. B. über "Add file" → "Upload files" direkt im Browser, kein Git-Wissen nötig).
2. In Vercel: "Add New… → Project" → das GitHub-Repository auswählen → "Deploy".
3. Nach dem ersten Deploy: im Vercel-Projekt unter
   "Settings → Environment Variables" eine neue Variable anlegen:
   - Name: `REPLICATE_API_TOKEN`
   - Wert: dein Replicate-API-Key (r8_...)
4. Einmal neu deployen (Vercel → "Deployments" → "..." → "Redeploy"),
   damit die Variable greift.
5. Die fertige URL sieht etwa so aus:
   `https://dein-projekt-name.vercel.app/api/generate`
   Diese URL in der App als Proxy-Adresse eintragen.
