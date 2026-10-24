# Publish the PurpleSentinel profile README

GitHub shows a profile README when a **public** repository has the exact same name as the username and contains a `README.md` at its root, on its default branch.

Your existing profile repository is `https://github.com/PurpleSentinel/PurpleSentinel`.

## Upload in the GitHub web interface

1. Open [PurpleSentinel/PurpleSentinel](https://github.com/PurpleSentinel/PurpleSentinel).
2. Upload `README.md` to the repository root.
3. Upload **both** `assets/banner.svg` and `assets/footer.svg` into the `assets/` folder, preserving the folder names.
4. Commit to the default branch (typically `main`).
5. Visit [github.com/PurpleSentinel](https://github.com/PurpleSentinel) to see the result.

## Upload with Git on Fedora

From a local directory containing this downloaded profile package:

```bash
git clone git@github.com:PurpleSentinel/PurpleSentinel.git
cp README.md PurpleSentinel/README.md
mkdir -p PurpleSentinel/assets
cp assets/*.svg PurpleSentinel/assets/
cd PurpleSentinel
git add README.md assets/
git commit -m "Add colourful GitHub profile README"
git push origin main
```

If the profile repository already contains a README or any custom assets, review and merge rather than overwriting blindly.

## Design and compatibility

- Theme: **electric purple** `#955DF5`, **teal** `#40E0D0`, and **navy** `#0A1021`.
- Section colours and logo-style labels use external `shields.io` images, not unsupported inline Markdown CSS.
- Main graphics are local SVG files, so they do not depend on third-party image hosting.
- All featured repositories are public, linked directly and described from their existing READMEs.
- The README is normal GitHub-flavoured Markdown plus GitHub-compatible HTML for alignment and layout.
- Do not paste standalone `<svg>` markup into `README.md`; link to SVG assets with `<img>` as in this package.

## Customisation

To change your title or tagline, edit the text in `assets/banner.svg`. To change your introductory text or which repositories appear, edit `README.md`. Edit badge colour hex values in the `shields.io` URLs. No build tooling is required.
