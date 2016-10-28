```
                         _
        /     _/_    /) //
   _   /_  __ /  __ // // __ , , ,
  /_)_/ /_(_)<__(_)//_</_(_)(_(_/_
 /                />
'                </
```

---

Photoflow is a small CLI that I use to manage my photography workflow. I'm very much an amateur and Photoflow provides an opinionated workflow for working with photos from multiple cameras and Google Photos.

And by an "opinionated workflow", I mean the following:

1. Set `PHOTOFLOW_IMPORT_DEST` to something meaningful. I set it to `/mnt/external/storage/photos`, which is on an external HDD I have that's automatically backed up.
2. Plug yer camera in and make sure it's the only plugged in camera
3. Run `photoflow import` to import all of your photos to `PHOTOFLOW_IMPORT_DEST/inbox`
4. Make all the edits you want, save them to the JPG files. Don't edit the RAW files. Leave WIP files, like PSDs, in the inbox with the same filename as the file they're editing. If I'm editing `DSCF1820.RAF` in Photoshop, I'd save the PSD as `DSCF1820.PSD` in the inbox and save the edits to `DSCF1820.JPG`, overwriting the original JPG.
5. Copy all of the JPGs from `PHOTOFLOW_IMPORT_DEST/inbox` to Google Photos
6. Run `photoflow move_from_inbox` to move all of your files from `PHOTOFLOW_IMPORT_DEST/inbox` to `PHOTOFLOW_IMPORT_DEST`. It's important that you don't `mv` these files manually, you _must_ run this command.
7. And you're done!

I do not recommend using Photoflow for your own use. It will suddenly change without notice and break your workflow. Instead, you should check out the code and build your own tooling that fits your workflow.

## License

See [`LICENSE`][LICENSE].
