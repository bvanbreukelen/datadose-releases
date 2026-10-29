# DataDose releases

`releases.json` is DataDose's update index: once a day, a DataDose server asks this file which version is the newest,
and its System page shows super admins whether an update is available, with its notes and the steps to take.

- **What a server sends:** only the request for this file, with a User-Agent naming its version. Nothing else.
- **Switching it off:** on DataDose's System page. A private mirror: `DATADOSE_UPDATE_INDEX` in `.env`.
- **The format:** `docs/releasing.md`, "The update index", in DataDose's repository. Entries are added with
  `npm run release-entry` there, never changed afterwards.
