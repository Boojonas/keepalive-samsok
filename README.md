# keepalive-samsok

Håller söktjänsten [Samsökning – Nätverket Sydväst](https://github.com/Boojonas/sydvast-samsokning) vaken på Streamlit Community Cloud.

Streamlit stänger av appar som inte haft besök på cirka 12 timmar, och det tar sedan en stund att väcka dem. Arbetsflödet i `.github/workflows/keepalive.yml` öppnar därför appen i en riktig webbläsare (Playwright) var fjärde timme, och klickar på "Yes, get this app back up!" om den ändå har somnat.

GitHub stänger av schemalagda arbetsflöden i publika repon efter 60 dagar utan aktivitet. Arbetsflödet återaktiverar sig därför självt vid varje körning.

Arbetsflödet kan också köras manuellt under fliken **Actions → Håll samsök-appen vaken → Run workflow**.
