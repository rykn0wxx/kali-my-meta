# Custom Kali Linux Metapackage



This is a custom build kali linux metapackages

> `kali-my-meta` includes several basic kali linux tools

### Build your own

Clone kali linux meta packages
```
git clone git@gitlab.com:kalilinux/packages/kali-meta.git
```
or
```
git clone https://gitlab.com/kalilinux/packages/kali-meta.git
```
Select tools or matapackages of your choice

```
cd kali-meta/debian
```

edit the **control** file, you may refer to the **control** file included on this repo as guide.

Once completed and definde, bump the version using `dch` and provided changes made

```
dch --local kohana
```

You may replace `kohana` with any word of your choice, as this will be included on the name of final build.

Finally, build the new metapackage with the `dpkg-buildpackage` command.
```
dpkg-buildpackage -us -uc -b
```
