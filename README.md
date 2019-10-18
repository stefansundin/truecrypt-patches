I use this repository to manage my patches for [truecrypt.deb](https://github.com/stefansundin/truecrypt.deb).

There is a different branch for each patch. It is easy to use git to create the patches which can then be used in the debianization.

```
for branch in 7.1a build-fixes gcc5 gcc6 wxWidgets indicator helpfix xdg-open open-doc update-urls mac
do
  git branch --track $branch origin/$branch
done

git diff 7.1a..build-fixes > ../truecrypt-7.1a-build-fixes.patch
git diff 7.1a..gcc5 > ../truecrypt-7.1a-gcc5.patch
git diff build-fixes..gcc6 > ../truecrypt-7.1a-gcc6.patch
git diff 7.1a..wxWidgets > ../truecrypt-7.1a-wxWidgets.patch
git diff build-fixes..indicator > ../truecrypt-7.1a-indicator.patch
git diff 7.1a..helpfix > ../truecrypt-7.1a-helpfix.patch
git diff 7.1a..xdg-open > ../truecrypt-7.1a-xdg-open.patch
git diff 7.1a..open-doc > ../truecrypt-7.1a-open-doc.patch
git diff 7.1a..update-urls > ../truecrypt-7.1a-update-urls.patch
git diff 7.1a..mac > ../truecrypt-7.1a-mac.patch
```

Web diffs:
- [7.1a..build-fixes](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..build-fixes)
- [7.1a..gcc5](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..gcc5)
- [build-fixes..gcc6](https://github.com/stefansundin/truecrypt-patches/compare/build-fixes..gcc6)
- [7.1a..wxWidgets](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..wxWidgets)
- [build-fixes..indicator](https://github.com/stefansundin/truecrypt-patches/compare/build-fixes..indicator)
- [7.1a..helpfix](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..helpfix)
- [7.1a..xdg-open](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..xdg-open)
- [7.1a..open-doc](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..open-doc)
- [7.1a..update-urls](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..update-urls)
- [7.1a..mac](https://github.com/stefansundin/truecrypt-patches/compare/7.1a..mac)
