# Comparing `tmp/music-assistant-frontend-2.0.6.tar.gz` & `tmp/music-assistant-frontend-2.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "music-assistant-frontend-2.0.6.tar", last modified: Sun Jul 23 19:35:06 2023, max compression
+gzip compressed data, was "music-assistant-frontend-2.0.7.tar", last modified: Sun Jul 23 19:40:54 2023, max compression
```

## Comparing `music-assistant-frontend-2.0.6.tar` & `music-assistant-frontend-2.0.7.tar`

### file list

```diff
@@ -1,164 +1,164 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:35:06.016995 music-assistant-frontend-2.0.6/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 19:33:38.000000 music-assistant-frontend-2.0.6/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       77 2023-07-23 19:33:38.000000 music-assistant-frontend-2.0.6/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2855 2023-07-23 19:35:06.016995 music-assistant-frontend-2.0.6/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2489 2023-07-23 19:33:38.000000 music-assistant-frontend-2.0.6/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:35:05.992993 music-assistant-frontend-2.0.6/music_assistant_frontend/
--rw-r--r--   0 runner    (1001) docker     (123)      155 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2742 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/apple-touch-icon.png
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:35:06.016995 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/
--rw-r--r--   0 runner    (1001) docker     (123)     2789 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/AddProvider-0b5f3371.js
--rw-r--r--   0 runner    (1001) docker     (123)     3178 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/AlbumDetails-8595c1ca.js
--rw-r--r--   0 runner    (1001) docker     (123)     3416 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Alert-eb81bdeb.js
--rw-r--r--   0 runner    (1001) docker     (123)     9174 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Alert-eefd31ea.css
--rw-r--r--   0 runner    (1001) docker     (123)     3319 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ArtistDetails-dcd8523b.js
--rw-r--r--   0 runner    (1001) docker     (123)     1886 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/BrowseView-c902aae4.js
--rw-r--r--   0 runner    (1001) docker     (123)      219 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Container-8440890a.css
--rw-r--r--   0 runner    (1001) docker     (123)      817 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Container-d623752d.js
--rw-r--r--   0 runner    (1001) docker     (123)     4899 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/CoreConfigs-6f585b64.js
--rw-r--r--   0 runner    (1001) docker     (123)     9160 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/CoreConfigs-fc1a0848.css
--rw-r--r--   0 runner    (1001) docker     (123)    67865 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Default-7a0e81ad.js
--rw-r--r--   0 runner    (1001) docker     (123)    17247 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Default-872711e9.css
--rw-r--r--   0 runner    (1001) docker     (123)     7161 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditConfig-0f6f6afc.css
--rw-r--r--   0 runner    (1001) docker     (123)    10291 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js
--rw-r--r--   0 runner    (1001) docker     (123)     2728 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditCoreConfig-e48660bd.js
--rw-r--r--   0 runner    (1001) docker     (123)     3250 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditPlayer-9b8c67de.js
--rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditProvider-f7b6707b.js
--rw-r--r--   0 runner    (1001) docker     (123)     1468 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/HomeView-297a9bbc.js
--rw-r--r--   0 runner    (1001) docker     (123)       82 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/HomeView-f559b858.css
--rw-r--r--   0 runner    (1001) docker     (123)     8261 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ItemsListing-9c236e22.css
--rw-r--r--   0 runner    (1001) docker     (123)    19333 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js
--rw-r--r--   0 runner    (1001) docker     (123)     1428 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxEIzIFKw-8007dfe8.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    14688 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxFIzIFKw-8e48cf20.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    11804 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxGIzIFKw-10b31f4c.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     5388 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxHIzIFKw-ca7eea0c.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15764 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxIIzI-0f303f31.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     7012 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxLIzIFKw-8c3798e3.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     9180 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxMIzIFKw-638764dc.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     9840 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fABc4EsA-3728fbdd.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15920 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBBc4-b0195382.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     7016 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBxc4EsA-713780d8.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1500 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCBc4EsA-ef8f0236.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    14968 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCRc4EsA-aeed0e51.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    11800 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fChc4EsA-7f1c829b.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     5604 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCxc4EsA-0948409a.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     9576 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fABc4EsA-47aa3bfa.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15740 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBBc4-f7591131.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     7120 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBxc4EsA-455c2c1a.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1480 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCBc4EsA-20dc200c.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15000 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCRc4EsA-435e4b7f.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    11796 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fChc4EsA-b076e863.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     5468 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCxc4EsA-51f3f418.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     9644 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfABc4EsA-6a84eeee.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15860 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBBc4-f5aebdfe.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     6936 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBxc4EsA-1c9cc76f.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCBc4EsA-5b6377da.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    14684 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCRc4EsA-3c505383.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    11824 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfChc4EsA-fc66f942.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     5548 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCxc4EsA-4ec57f2a.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     9700 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfABc4EsA-9fdb12ce.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15752 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBBc4-7e262106.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     7040 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBxc4EsA-2550c2e2.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1464 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCBc4EsA-76da333a.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    14856 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCRc4EsA-f265cee6.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    11756 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfChc4EsA-2781e9e7.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     5468 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCxc4EsA-3a38c967.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     7112 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4WxKOzY-daf51ab5.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4mxK-f6734f81.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     9628 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu5mxKOzY-495d38d4.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    15344 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu72xKOzY-b7ef2cd1.woff2
--rw-r--r--   0 runner    (1001) docker     (123)    11872 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7GxKOzY-3c23eb02.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     5560 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7WxKOzY-77b24796.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1484 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7mxKOzY-d368cf5b.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryAlbums-e581ef5e.js
--rw-r--r--   0 runner    (1001) docker     (123)     1763 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryArtists-b9bf1b9d.js
--rw-r--r--   0 runner    (1001) docker     (123)     2266 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryPlaylists-b4797965.js
--rw-r--r--   0 runner    (1001) docker     (123)     2137 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryRadios-31300560.js
--rw-r--r--   0 runner    (1001) docker     (123)     2214 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryTracks-676be9ae.js
--rw-r--r--   0 runner    (1001) docker     (123)      758 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListItem-3da12b03.css
--rw-r--r--   0 runner    (1001) docker     (123)     3475 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListItem-6dad7331.js
--rw-r--r--   0 runner    (1001) docker     (123)    25774 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListviewItem-2c46c8ee.js
--rw-r--r--   0 runner    (1001) docker     (123)     6117 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListviewItem-54a3402d.css
--rw-r--r--   0 runner    (1001) docker     (123)   160576 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-11ec382a.woff
--rw-r--r--   0 runner    (1001) docker     (123)   347588 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-29c11fa5.ttf
--rw-r--r--   0 runner    (1001) docker     (123)   125116 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-5743ed3d.woff2
--rw-r--r--   0 runner    (1001) docker     (123)   143452 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-e69d687a.eot
--rw-r--r--   0 runner    (1001) docker     (123)      512 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MediaItemThumb-5ee47663.css
--rw-r--r--   0 runner    (1001) docker     (123)    28715 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js
--rw-r--r--   0 runner    (1001) docker     (123)      277 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PanelviewItem-14a6b77a.css
--rw-r--r--   0 runner    (1001) docker     (123)     3418 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js
--rw-r--r--   0 runner    (1001) docker     (123)     8888 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PlayerQueue-41b4928f.js
--rw-r--r--   0 runner    (1001) docker     (123)     3178 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Players-525b85bc.js
--rw-r--r--   0 runner    (1001) docker     (123)     2149 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PlaylistDetails-cce72360.js
--rw-r--r--   0 runner    (1001) docker     (123)     5121 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ProviderDetails-da7f4c54.css
--rw-r--r--   0 runner    (1001) docker     (123)     9305 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js
--rw-r--r--   0 runner    (1001) docker     (123)     5232 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Providers-3598c1f3.js
--rw-r--r--   0 runner    (1001) docker     (123)       43 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Providers-3820a270.css
--rw-r--r--   0 runner    (1001) docker     (123)     2054 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/RadioDetails-993d50b0.js
--rw-r--r--   0 runner    (1001) docker     (123)     4957 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Search-433484bb.js
--rw-r--r--   0 runner    (1001) docker     (123)     1165 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Settings-70d67eb6.js
--rw-r--r--   0 runner    (1001) docker     (123)     3371 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/TrackDetails-95dc4644.js
--rw-r--r--   0 runner    (1001) docker     (123)     6101 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBadge-4ff04865.css
--rw-r--r--   0 runner    (1001) docker     (123)     1905 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBadge-8be61727.js
--rw-r--r--   0 runner    (1001) docker     (123)    31740 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBtn-a0da5efe.js
--rw-r--r--   0 runner    (1001) docker     (123)    25020 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBtn-fccecd75.css
--rw-r--r--   0 runner    (1001) docker     (123)     4348 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCard-111cabcf.js
--rw-r--r--   0 runner    (1001) docker     (123)    11304 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCard-790bb5b3.css
--rw-r--r--   0 runner    (1001) docker     (123)    17528 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCheckboxBtn-d54a899d.js
--rw-r--r--   0 runner    (1001) docker     (123)    21750 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCheckboxBtn-e9f604b5.css
--rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VDialog-ccbfddc9.js
--rw-r--r--   0 runner    (1001) docker     (123)     6659 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VDialog-ff1232cf.css
--rw-r--r--   0 runner    (1001) docker     (123)    25078 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VExpansionPanel-286d9c63.js
--rw-r--r--   0 runner    (1001) docker     (123)    23455 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VExpansionPanel-2b4b0a5a.css
--rw-r--r--   0 runner    (1001) docker     (123)    23282 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VGrid-ec674b79.css
--rw-r--r--   0 runner    (1001) docker     (123)    17105 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VListItem-028a8916.css
--rw-r--r--   0 runner    (1001) docker     (123)    11172 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VListItem-943ee224.js
--rw-r--r--   0 runner    (1001) docker     (123)    32757 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VMenu-3bdd1b96.js
--rw-r--r--   0 runner    (1001) docker     (123)     9341 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VMenu-87d759b1.css
--rw-r--r--   0 runner    (1001) docker     (123)     2913 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VRow-73379099.js
--rw-r--r--   0 runner    (1001) docker     (123)      101 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VSpacer-4e341220.js
--rw-r--r--   0 runner    (1001) docker     (123)     8837 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTabs-7c03bdc8.js
--rw-r--r--   0 runner    (1001) docker     (123)     7678 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTabs-f9f04fad.css
--rw-r--r--   0 runner    (1001) docker     (123)    23046 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTextField-6adde8bb.css
--rw-r--r--   0 runner    (1001) docker     (123)     9279 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTextField-f81f9175.js
--rw-r--r--   0 runner    (1001) docker     (123)     7610 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VToolbar-aa2d1d9a.css
--rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VToolbar-dfba6de4.js
--rw-r--r--   0 runner    (1001) docker     (123)     3572 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/contextmenu-ec34ccac.js
--rw-r--r--   0 runner    (1001) docker     (123)    11926 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/cover_dark-75402cd0.png
--rw-r--r--   0 runner    (1001) docker     (123)    11831 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/cover_light-b832ae9e.png
--rw-r--r--   0 runner    (1001) docker     (123)     4214 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/crossfade-ba51f69a.png
--rw-r--r--   0 runner    (1001) docker     (123)      329 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/eventbus-d154090d.js
--rw-r--r--   0 runner    (1001) docker     (123)    16057 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/hires-438c7046.png
--rw-r--r--   0 runner    (1001) docker     (123)     4339 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index-0afee102.js
--rw-r--r--   0 runner    (1001) docker     (123)   663392 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index-4bf8ac1c.css
--rw-r--r--   0 runner    (1001) docker     (123)   411590 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index-dcf0de03.js
--rw-r--r--   0 runner    (1001) docker     (123)      184 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index.browser-7e542916.js
--rw-r--r--   0 runner    (1001) docker     (123)    28226 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/info_gradient-a4aefd1d.jpg
--rw-r--r--   0 runner    (1001) docker     (123)     4302 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/layout-087be267.js
--rw-r--r--   0 runner    (1001) docker     (123)    15778 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/logo-c9d5d6ab.png
--rw-r--r--   0 runner    (1001) docker     (123)     9150 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/m4a-45331b05.png
--rw-r--r--   0 runner    (1001) docker     (123)   155276 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/material-icons-outlined-35dca8a7.woff2
--rw-r--r--   0 runner    (1001) docker     (123)  1280212 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-67d24abe.eot
--rw-r--r--   0 runner    (1001) docker     (123)   576748 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-80bb28b3.woff
--rw-r--r--   0 runner    (1001) docker     (123)  1279992 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-a58ecb54.ttf
--rw-r--r--   0 runner    (1001) docker     (123)   396732 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-c1c004a9.woff2
--rw-r--r--   0 runner    (1001) docker     (123)     1220 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/vue-virtual-scroller-4d71315f.css
--rw-r--r--   0 runner    (1001) docker     (123)     5289 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/assets/workbox-window.prod.es5-a7b12eab.js
--rw-r--r--   0 runner    (1001) docker     (123)    15086 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/favicon.ico
--rw-r--r--   0 runner    (1001) docker     (123)      989 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/favicon.svg
--rw-r--r--   0 runner    (1001) docker     (123)    11942 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/index.html
--rw-r--r--   0 runner    (1001) docker     (123)      563 2023-07-23 19:34:51.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/manifest.webmanifest
--rw-r--r--   0 runner    (1001) docker     (123)     7543 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/pwa-192x192.png
--rw-r--r--   0 runner    (1001) docker     (123)     7883 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/pwa-512x512.png
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 19:34:48.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/robots.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5685 2023-07-23 19:34:54.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/sw.js
--rw-r--r--   0 runner    (1001) docker     (123)    14986 2023-07-23 19:34:54.000000 music-assistant-frontend-2.0.6/music_assistant_frontend/workbox-27b29e6f.js
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:35:05.992993 music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2855 2023-07-23 19:35:05.000000 music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9389 2023-07-23 19:35:05.000000 music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:35:05.000000 music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:35:03.000000 music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-23 19:35:05.000000 music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      651 2023-07-23 19:34:06.000000 music-assistant-frontend-2.0.6/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:35:06.016995 music-assistant-frontend-2.0.6/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:40:54.353668 music-assistant-frontend-2.0.7/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 19:39:36.000000 music-assistant-frontend-2.0.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       77 2023-07-23 19:39:36.000000 music-assistant-frontend-2.0.7/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2855 2023-07-23 19:40:54.353668 music-assistant-frontend-2.0.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2489 2023-07-23 19:39:36.000000 music-assistant-frontend-2.0.7/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:40:54.329667 music-assistant-frontend-2.0.7/music_assistant_frontend/
+-rw-r--r--   0 runner    (1001) docker     (123)      155 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2742 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/apple-touch-icon.png
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:40:54.353668 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/
+-rw-r--r--   0 runner    (1001) docker     (123)     2789 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/AddProvider-1cb2a794.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3178 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/AlbumDetails-28f977b9.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3416 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Alert-bdc4de4a.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9174 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Alert-eefd31ea.css
+-rw-r--r--   0 runner    (1001) docker     (123)     3319 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ArtistDetails-b3bb2766.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1886 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/BrowseView-dc407ea0.js
+-rw-r--r--   0 runner    (1001) docker     (123)      817 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Container-32d4da6e.js
+-rw-r--r--   0 runner    (1001) docker     (123)      219 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Container-8440890a.css
+-rw-r--r--   0 runner    (1001) docker     (123)     4909 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/CoreConfigs-f7edf5eb.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9160 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/CoreConfigs-fc1a0848.css
+-rw-r--r--   0 runner    (1001) docker     (123)    17247 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Default-872711e9.css
+-rw-r--r--   0 runner    (1001) docker     (123)    67865 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Default-e0bfb99e.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7161 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditConfig-0f6f6afc.css
+-rw-r--r--   0 runner    (1001) docker     (123)    10291 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditConfig.vue_vue_type_style_index_0_lang-74792501.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2728 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditCoreConfig-b660ec39.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3250 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditPlayer-7719345f.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditProvider-7ffddf94.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1468 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/HomeView-eae672c0.js
+-rw-r--r--   0 runner    (1001) docker     (123)       82 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/HomeView-f559b858.css
+-rw-r--r--   0 runner    (1001) docker     (123)     8261 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ItemsListing-9c236e22.css
+-rw-r--r--   0 runner    (1001) docker     (123)    19333 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1428 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxEIzIFKw-8007dfe8.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    14688 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxFIzIFKw-8e48cf20.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    11804 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxGIzIFKw-10b31f4c.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     5388 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxHIzIFKw-ca7eea0c.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15764 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxIIzI-0f303f31.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     7012 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxLIzIFKw-8c3798e3.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     9180 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxMIzIFKw-638764dc.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     9840 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fABc4EsA-3728fbdd.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15920 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBBc4-b0195382.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     7016 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBxc4EsA-713780d8.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1500 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCBc4EsA-ef8f0236.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    14968 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCRc4EsA-aeed0e51.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    11800 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fChc4EsA-7f1c829b.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     5604 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCxc4EsA-0948409a.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     9576 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fABc4EsA-47aa3bfa.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15740 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBBc4-f7591131.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     7120 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBxc4EsA-455c2c1a.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1480 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCBc4EsA-20dc200c.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15000 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCRc4EsA-435e4b7f.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    11796 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fChc4EsA-b076e863.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     5468 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCxc4EsA-51f3f418.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     9644 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfABc4EsA-6a84eeee.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15860 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBBc4-f5aebdfe.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     6936 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBxc4EsA-1c9cc76f.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCBc4EsA-5b6377da.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    14684 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCRc4EsA-3c505383.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    11824 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfChc4EsA-fc66f942.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     5548 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCxc4EsA-4ec57f2a.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     9700 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfABc4EsA-9fdb12ce.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15752 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBBc4-7e262106.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     7040 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBxc4EsA-2550c2e2.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1464 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCBc4EsA-76da333a.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    14856 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCRc4EsA-f265cee6.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    11756 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfChc4EsA-2781e9e7.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     5468 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCxc4EsA-3a38c967.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     7112 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4WxKOzY-daf51ab5.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15744 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4mxK-f6734f81.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     9628 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu5mxKOzY-495d38d4.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    15344 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu72xKOzY-b7ef2cd1.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)    11872 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7GxKOzY-3c23eb02.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     5560 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7WxKOzY-77b24796.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1484 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7mxKOzY-d368cf5b.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryAlbums-cc4c5558.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1763 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryArtists-be2722d0.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2266 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryPlaylists-14676281.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2137 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryRadios-d371d843.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2214 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryTracks-ecb94887.js
+-rw-r--r--   0 runner    (1001) docker     (123)      758 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListItem-3da12b03.css
+-rw-r--r--   0 runner    (1001) docker     (123)     3475 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListItem-bba986fb.js
+-rw-r--r--   0 runner    (1001) docker     (123)     6117 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListviewItem-54a3402d.css
+-rw-r--r--   0 runner    (1001) docker     (123)    25774 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListviewItem-ade956db.js
+-rw-r--r--   0 runner    (1001) docker     (123)   160576 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-11ec382a.woff
+-rw-r--r--   0 runner    (1001) docker     (123)   347588 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-29c11fa5.ttf
+-rw-r--r--   0 runner    (1001) docker     (123)   125116 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-5743ed3d.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)   143452 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-e69d687a.eot
+-rw-r--r--   0 runner    (1001) docker     (123)      512 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MediaItemThumb-5ee47663.css
+-rw-r--r--   0 runner    (1001) docker     (123)    28715 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js
+-rw-r--r--   0 runner    (1001) docker     (123)      277 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PanelviewItem-14a6b77a.css
+-rw-r--r--   0 runner    (1001) docker     (123)     3418 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8888 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PlayerQueue-8c871ec2.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3178 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Players-2ae3919d.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2149 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PlaylistDetails-971d8698.js
+-rw-r--r--   0 runner    (1001) docker     (123)     5121 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ProviderDetails-da7f4c54.css
+-rw-r--r--   0 runner    (1001) docker     (123)     9305 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js
+-rw-r--r--   0 runner    (1001) docker     (123)       43 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Providers-3820a270.css
+-rw-r--r--   0 runner    (1001) docker     (123)     5232 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Providers-453e3025.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2054 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/RadioDetails-6761105c.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4957 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Search-93fe9303.js
+-rw-r--r--   0 runner    (1001) docker     (123)     1165 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Settings-ef547e38.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3371 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/TrackDetails-807370a0.js
+-rw-r--r--   0 runner    (1001) docker     (123)     6101 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBadge-4ff04865.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1905 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBadge-8b6f3afa.js
+-rw-r--r--   0 runner    (1001) docker     (123)    31740 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBtn-49774b84.js
+-rw-r--r--   0 runner    (1001) docker     (123)    25020 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBtn-fccecd75.css
+-rw-r--r--   0 runner    (1001) docker     (123)    11304 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCard-790bb5b3.css
+-rw-r--r--   0 runner    (1001) docker     (123)     4348 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCard-e81591ba.js
+-rw-r--r--   0 runner    (1001) docker     (123)    17528 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCheckboxBtn-4c08e900.js
+-rw-r--r--   0 runner    (1001) docker     (123)    21750 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCheckboxBtn-e9f604b5.css
+-rw-r--r--   0 runner    (1001) docker     (123)     1794 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VDialog-b35e6970.js
+-rw-r--r--   0 runner    (1001) docker     (123)     6659 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VDialog-ff1232cf.css
+-rw-r--r--   0 runner    (1001) docker     (123)    23455 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VExpansionPanel-2b4b0a5a.css
+-rw-r--r--   0 runner    (1001) docker     (123)    25078 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VExpansionPanel-523a6df6.js
+-rw-r--r--   0 runner    (1001) docker     (123)    23282 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VGrid-ec674b79.css
+-rw-r--r--   0 runner    (1001) docker     (123)    17105 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VListItem-028a8916.css
+-rw-r--r--   0 runner    (1001) docker     (123)    11172 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VListItem-b049d12d.js
+-rw-r--r--   0 runner    (1001) docker     (123)     9341 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VMenu-87d759b1.css
+-rw-r--r--   0 runner    (1001) docker     (123)    32757 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VMenu-a805d6b6.js
+-rw-r--r--   0 runner    (1001) docker     (123)     2913 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VRow-08fca7f1.js
+-rw-r--r--   0 runner    (1001) docker     (123)      101 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VSpacer-b8926de0.js
+-rw-r--r--   0 runner    (1001) docker     (123)     8837 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTabs-1b99b0fa.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7678 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTabs-f9f04fad.css
+-rw-r--r--   0 runner    (1001) docker     (123)    23046 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTextField-6adde8bb.css
+-rw-r--r--   0 runner    (1001) docker     (123)     9279 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTextField-be284f64.js
+-rw-r--r--   0 runner    (1001) docker     (123)     7610 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VToolbar-aa2d1d9a.css
+-rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VToolbar-b4c95f12.js
+-rw-r--r--   0 runner    (1001) docker     (123)     3572 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/contextmenu-7e32a8e5.js
+-rw-r--r--   0 runner    (1001) docker     (123)    11926 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/cover_dark-75402cd0.png
+-rw-r--r--   0 runner    (1001) docker     (123)    11831 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/cover_light-b832ae9e.png
+-rw-r--r--   0 runner    (1001) docker     (123)     4214 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/crossfade-ba51f69a.png
+-rw-r--r--   0 runner    (1001) docker     (123)      329 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/eventbus-d154090d.js
+-rw-r--r--   0 runner    (1001) docker     (123)    16057 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/hires-438c7046.png
+-rw-r--r--   0 runner    (1001) docker     (123)   663392 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index-4bf8ac1c.css
+-rw-r--r--   0 runner    (1001) docker     (123)   411590 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index-8ef8125d.js
+-rw-r--r--   0 runner    (1001) docker     (123)     4339 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index-a4f9d82d.js
+-rw-r--r--   0 runner    (1001) docker     (123)      184 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index.browser-7e542916.js
+-rw-r--r--   0 runner    (1001) docker     (123)    28226 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/info_gradient-a4aefd1d.jpg
+-rw-r--r--   0 runner    (1001) docker     (123)     4302 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/layout-2c008654.js
+-rw-r--r--   0 runner    (1001) docker     (123)    15778 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/logo-c9d5d6ab.png
+-rw-r--r--   0 runner    (1001) docker     (123)     9150 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/m4a-45331b05.png
+-rw-r--r--   0 runner    (1001) docker     (123)   155276 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/material-icons-outlined-35dca8a7.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)  1280212 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-67d24abe.eot
+-rw-r--r--   0 runner    (1001) docker     (123)   576748 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-80bb28b3.woff
+-rw-r--r--   0 runner    (1001) docker     (123)  1279992 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-a58ecb54.ttf
+-rw-r--r--   0 runner    (1001) docker     (123)   396732 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-c1c004a9.woff2
+-rw-r--r--   0 runner    (1001) docker     (123)     1220 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/vue-virtual-scroller-4d71315f.css
+-rw-r--r--   0 runner    (1001) docker     (123)     5289 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/assets/workbox-window.prod.es5-a7b12eab.js
+-rw-r--r--   0 runner    (1001) docker     (123)    15086 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/favicon.ico
+-rw-r--r--   0 runner    (1001) docker     (123)      989 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/favicon.svg
+-rw-r--r--   0 runner    (1001) docker     (123)    11942 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/index.html
+-rw-r--r--   0 runner    (1001) docker     (123)      563 2023-07-23 19:40:41.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/manifest.webmanifest
+-rw-r--r--   0 runner    (1001) docker     (123)     7543 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/pwa-192x192.png
+-rw-r--r--   0 runner    (1001) docker     (123)     7883 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/pwa-512x512.png
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 19:40:38.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/robots.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5685 2023-07-23 19:40:44.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/sw.js
+-rw-r--r--   0 runner    (1001) docker     (123)    14986 2023-07-23 19:40:44.000000 music-assistant-frontend-2.0.7/music_assistant_frontend/workbox-27b29e6f.js
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:40:54.333667 music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2855 2023-07-23 19:40:53.000000 music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9389 2023-07-23 19:40:54.000000 music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:40:53.000000 music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:40:52.000000 music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-23 19:40:54.000000 music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      651 2023-07-23 19:40:04.000000 music-assistant-frontend-2.0.7/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:40:54.353668 music-assistant-frontend-2.0.7/setup.cfg
```

### Comparing `music-assistant-frontend-2.0.6/LICENSE` & `music-assistant-frontend-2.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/PKG-INFO` & `music-assistant-frontend-2.0.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: music-assistant-frontend
-Version: 2.0.6
+Version: 2.0.7
 Summary: The Music Assistant frontend
 Author-email: The Music Assistant Authors <m.vanderveldt@outlook.com>
 License: Apache-2.0
 Project-URL: Homepage, https://github.com/music-assistant/frontend
 Platform: any
 Requires-Python: >=3.9.0
 Description-Content-Type: text/markdown
```

### Comparing `music-assistant-frontend-2.0.6/README.md` & `music-assistant-frontend-2.0.7/README.md`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/apple-touch-icon.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/apple-touch-icon.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/AddProvider-0b5f3371.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/AddProvider-1cb2a794.js`

 * *Files 5% similar despite different names*

#### js-beautify {}

```diff
@@ -16,37 +16,37 @@
     y as l,
     q as a,
     N as c,
     J as d,
     x as h,
     I as r,
     D as v
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as T
-} from "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js";
+} from "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js";
 import {
     c as $,
     b as _,
     V as j
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     b as A,
     e as D
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     x as I
-} from "./VBtn-a0da5efe.js";
-import "./VExpansionPanel-286d9c63.js";
-import "./VTextField-f81f9175.js";
-import "./index-0afee102.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VListItem-943ee224.js";
-import "./VSpacer-4e341220.js";
-import "./VDialog-ccbfddc9.js";
+} from "./VBtn-49774b84.js";
+import "./VExpansionPanel-523a6df6.js";
+import "./VTextField-be284f64.js";
+import "./index-a4f9d82d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VListItem-b049d12d.js";
+import "./VSpacer-b8926de0.js";
+import "./VDialog-b35e6970.js";
 const U = {
         key: 0,
         style: {
             "margin-left": "-5px",
             "margin-right": "-5px"
         }
     },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/AlbumDetails-8595c1ca.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/AlbumDetails-28f977b9.js`

 * *Files 7% similar despite different names*

#### js-beautify {}

```diff
@@ -1,15 +1,15 @@
 import {
     _ as v,
     f as c
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     _ as w,
     a as A
-} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js";
+} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js";
 import {
     l as g,
     r as f,
     c as I,
     aq as p,
     w as V,
     o as D,
@@ -18,35 +18,35 @@
     b as B,
     v as n,
     A as E,
     j as T,
     x as m,
     D as d,
     I as b
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
-import "./layout-087be267.js";
-import "./VDialog-ccbfddc9.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
+import "./layout-2c008654.js";
+import "./VDialog-b35e6970.js";
 const $ = b("br", null, null, -1),
     F = b("br", null, null, -1),
     ae = g({
         __name: "AlbumDetails",
         props: {
             itemId: {},
             provider: {},
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Alert-eb81bdeb.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Alert-bdc4de4a.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -12,21 +12,21 @@
     k,
     v as R,
     x as H,
     W as O,
     B as J,
     y as K,
     Z as M
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     a as N
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     d as W
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     a as Z,
     n as q,
     J as G,
     b as Q,
     y as U,
     z as X,
@@ -41,15 +41,15 @@
     C as re,
     g as ie,
     H as ce,
     E as ue,
     j as de,
     F as f,
     V as ve
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 const me = W("v-alert-title"),
     ye = ["success", "info", "warning", "error"],
     fe = T({
         border: {
             type: [Boolean, String],
             validator: e => typeof e == "boolean" || ["top", "end", "bottom", "start"].includes(e)
         },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Alert-eefd31ea.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Alert-eefd31ea.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ArtistDetails-dcd8523b.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ArtistDetails-b3bb2766.js`

 * *Files 10% similar despite different names*

#### js-beautify {}

```diff
@@ -1,15 +1,15 @@
 import {
     _,
     f as b
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     _ as h,
     a as g
-} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js";
+} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js";
 import {
     l as D,
     r as u,
     w as I,
     o as E,
     H as a,
     ao as F,
@@ -18,35 +18,35 @@
     aq as m,
     v as l,
     A as B,
     j as $,
     x as d,
     D as v,
     I as y
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
-import "./layout-087be267.js";
-import "./VDialog-ccbfddc9.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
+import "./layout-2c008654.js";
+import "./VDialog-b35e6970.js";
 const C = y("br", null, null, -1),
     N = y("br", null, null, -1),
     oe = D({
         __name: "ArtistDetails",
         props: {
             itemId: {},
             provider: {}
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/BrowseView-c902aae4.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/BrowseView-dc407ea0.js`

 * *Files 18% similar despite different names*

#### js-beautify {}

```diff
@@ -13,40 +13,40 @@
     J as d,
     q as v,
     D as l,
     x as h,
     H as C,
     M as D,
     an as L
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     L as N,
     s as x
-} from "./ListviewItem-2c46c8ee.js"; /* empty css                             */
+} from "./ListviewItem-ade956db.js"; /* empty css                             */
 import {
     C as M
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     V as T
-} from "./VBadge-8be61727.js";
+} from "./VBadge-8b6f3afa.js";
 import {
     V as $
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     b as q
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     k as E
-} from "./VBtn-a0da5efe.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./index-0afee102.js";
-import "./VCard-111cabcf.js"; /* empty css              */
+} from "./VBtn-49774b84.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./index-a4f9d82d.js";
+import "./VCard-e81591ba.js"; /* empty css              */
 const F = {
         key: 0
     },
     Y = _({
         __name: "BrowseView",
         props: {
             path: {}
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Container-d623752d.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Container-32d4da6e.js`

 * *Files 5% similar despite different names*

#### js-beautify {}

```diff
@@ -7,23 +7,23 @@
     v as p,
     x as u,
     W as d,
     B as f,
     k as m,
     y as _,
     Z as C
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     a as v
-} from "./ListItem-6dad7331.js"; /* empty css              */
+} from "./ListItem-bba986fb.js"; /* empty css              */
 import {
     a as y,
     d as P,
     i as g
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 const k = {
     setup(e, s) {
         const t = n(() => ({}));
         return {
             containerProps: n(() => ({
                 ...t.value,
                 ...s.attrs
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/CoreConfigs-6f585b64.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/CoreConfigs-f7edf5eb.js`

 * *Files 6% similar despite different names*

#### js-beautify {}

```diff
@@ -11,86 +11,86 @@
     o as q,
     H as s,
     Q as z,
     af as E,
     v as b,
     A as y,
     I as e,
-    y as r,
+    y as d,
     N as k,
     J as t,
     F as L,
     B as J,
-    q as d,
+    q as i,
     D as T,
     R as Q,
     x as V
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     L as G,
     _ as K
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     C as B
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     V as I
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     b as A
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     a as O,
     n as W,
     d as X,
     p as Y,
     i as Z,
     j as D
-} from "./VBtn-a0da5efe.js";
-import "./VListItem-943ee224.js"; /* empty css              */
-import "./index-0afee102.js";
+} from "./VBtn-49774b84.js";
+import "./VListItem-b049d12d.js"; /* empty css              */
+import "./index-a4f9d82d.js";
 const ee = F({
         fixedHeader: Boolean,
         fixedFooter: Boolean,
         height: [Number, String],
         hover: Boolean,
         ...O(),
         ...W(),
         ...X(),
         ...R()
     }, "VTable"),
     te = x()({
         name: "VTable",
         props: ee(),
-        setup(i, p) {
+        setup(r, p) {
             let {
                 slots: n
             } = p;
             const {
                 themeClasses: f
-            } = H(i), {
+            } = H(r), {
                 densityClasses: _
-            } = Y(i);
-            return Z(() => l(i.tag, {
+            } = Y(r);
+            return Z(() => l(r.tag, {
                 class: ["v-table", {
-                    "v-table--fixed-height": !!i.height,
-                    "v-table--fixed-header": i.fixedHeader,
-                    "v-table--fixed-footer": i.fixedFooter,
+                    "v-table--fixed-height": !!r.height,
+                    "v-table--fixed-header": r.fixedHeader,
+                    "v-table--fixed-footer": r.fixedFooter,
                     "v-table--has-top": !!n.top,
                     "v-table--has-bottom": !!n.bottom,
-                    "v-table--hover": i.hover
-                }, f.value, _.value, i.class],
-                style: i.style
+                    "v-table--hover": r.hover
+                }, f.value, _.value, r.class],
+                style: r.style
             }, {
                 default: () => {
                     var m, v, c;
                     return [(m = n.top) == null ? void 0 : m.call(n), n.default ? l("div", {
                         class: "v-table__wrapper",
                         style: {
-                            height: j(i.height)
+                            height: j(r.height)
                         }
                     }, [l("table", null, [n.default()])]) : (v = n.wrapper) == null ? void 0 : v.call(n), (c = n.bottom) == null ? void 0 : c.call(n)]
                 }
             })), {}
         }
     }),
     ae = {
@@ -108,21 +108,18 @@
         style: {
             "margin-bottom": "10px"
         }
     },
     le = {
         key: 0
     },
-    ie = {
-        href: "${api.baseUrl}/log",
-        target: "_blank"
-    },
+    ie = ["href"],
     pe = S({
         __name: "CoreConfigs",
-        setup(i) {
+        setup(r) {
             const p = U(),
                 n = u([]),
                 f = u(0),
                 _ = u(0),
                 m = u(0),
                 v = u(0),
                 c = u(0),
@@ -139,58 +136,58 @@
                     P = E("hold");
                 return b(), y(L, null, [e("div", ae, [l(I, {
                     color: "transparent",
                     style: {
                         height: "55px"
                     }
                 }, {
-                    title: r(() => [k(t(a.$t("settings.settings")) + " | " + t(a.$t("settings.core_modules")), 1)]),
+                    title: d(() => [k(t(a.$t("settings.settings")) + " | " + t(a.$t("settings.core_modules")), 1)]),
                     _: 1
                 }), l(A), l(B, null, {
-                    default: r(() => [(b(!0), y(L, null, J(n.value.sort((o, g) => d(s).providerManifests[o.domain].name.localeCompare(d(s).providerManifests[g.domain].name)), o => Q((b(), V(G, {
+                    default: d(() => [(b(!0), y(L, null, J(n.value.sort((o, g) => i(s).providerManifests[o.domain].name.localeCompare(i(s).providerManifests[g.domain].name)), o => Q((b(), V(G, {
                         key: o.domain,
                         class: "list-item-main",
                         link: "",
                         "context-menu-items": [{
                             label: "settings.configure",
                             labelArgs: [],
                             action: () => {
                                 h(o.domain)
                             },
                             icon: "mdi-cog"
                         }, {
                             label: "settings.documentation",
                             labelArgs: [],
                             action: () => {
-                                M(d(s).providerManifests[o.domain].documentation)
+                                M(i(s).providerManifests[o.domain].documentation)
                             },
                             icon: "mdi-bookshelf",
-                            disabled: !d(s).providerManifests[o.domain].documentation
+                            disabled: !i(s).providerManifests[o.domain].documentation
                         }],
                         onClick: g => h(o.domain)
                     }, {
-                        prepend: r(() => [l(K, {
+                        prepend: d(() => [l(K, {
                             domain: o.domain,
                             size: 40,
                             class: "listitem-media-thumb",
                             style: {
                                 "margin-left": "10px"
                             }
                         }, null, 8, ["domain"])]),
-                        title: r(() => [e("div", se, t(d(s).providerManifests[o.domain].name), 1)]),
-                        subtitle: r(() => [e("div", ne, t(d(s).providerManifests[o.domain].description), 1)]),
-                        append: r(() => [o.last_error ? (b(), V(N, {
+                        title: d(() => [e("div", se, t(i(s).providerManifests[o.domain].name), 1)]),
+                        subtitle: d(() => [e("div", ne, t(i(s).providerManifests[o.domain].description), 1)]),
+                        append: d(() => [o.last_error ? (b(), V(N, {
                             key: 0,
                             icon: "",
                             title: o.last_error
                         }, {
-                            default: r(() => [l(D, {
+                            default: d(() => [l(D, {
                                 color: "red"
                             }, {
-                                default: r(() => [k(" mdi-alert-circle ")]),
+                                default: d(() => [k(" mdi-alert-circle ")]),
                                 _: 1
                             })]),
                             _: 2
                         }, 1032, ["title"])) : T("", !0)]),
                         _: 2
                     }, 1032, ["context-menu-items", "onClick"])), [
                         [P, () => {
@@ -200,23 +197,26 @@
                     _: 1
                 })]), e("div", oe, [l(I, {
                     color: "transparent",
                     style: {
                         height: "55px"
                     }
                 }, {
-                    title: r(() => [k(t(a.$t("settings.settings")) + " | " + t(a.$t("settings.server_info")), 1)]),
+                    title: d(() => [k(t(a.$t("settings.settings")) + " | " + t(a.$t("settings.server_info")), 1)]),
                     _: 1
                 }), l(A), l(B, null, {
-                    default: r(() => [l(te, null, {
-                        default: r(() => {
+                    default: d(() => [l(te, null, {
+                        default: d(() => {
                             var o, g, C, $, w;
-                            return [e("tbody", null, [e("tr", null, [e("td", null, t(a.$t("settings.server_id")), 1), e("td", null, t((o = d(s).serverInfo.value) == null ? void 0 : o.server_id), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.server_version")), 1), e("td", null, t((g = d(s).serverInfo.value) == null ? void 0 : g.server_version), 1)]), (C = d(s).serverInfo.value) != null && C.homeassistant_addon ? T("", !0) : (b(), y("tr", le, [e("td", null, t(a.$t("settings.server_base_url")), 1), e("td", null, t(($ = d(s).serverInfo.value) == null ? void 0 : $.base_url), 1)])), e("tr", null, [e("td", null, t(a.$t("settings.server_as_addon")), 1), e("td", null, [l(D, {
-                                icon: (w = d(s).serverInfo.value) != null && w.homeassistant_addon ? "mdi-check" : "mdi-close"
-                            }, null, 8, ["icon"])])]), e("tr", null, [e("td", null, t(a.$t("settings.artists_in_library")), 1), e("td", null, t(f.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.albums_in_library")), 1), e("td", null, t(_.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.tracks_in_library")), 1), e("td", null, t(m.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.playlists_in_library")), 1), e("td", null, t(v.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.radio_in_library")), 1), e("td", null, t(c.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.server_logging")), 1), e("td", null, [e("a", ie, t(a.$t("settings.download_log")), 1)])])])]
+                            return [e("tbody", null, [e("tr", null, [e("td", null, t(a.$t("settings.server_id")), 1), e("td", null, t((o = i(s).serverInfo.value) == null ? void 0 : o.server_id), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.server_version")), 1), e("td", null, t((g = i(s).serverInfo.value) == null ? void 0 : g.server_version), 1)]), (C = i(s).serverInfo.value) != null && C.homeassistant_addon ? T("", !0) : (b(), y("tr", le, [e("td", null, t(a.$t("settings.server_base_url")), 1), e("td", null, t(($ = i(s).serverInfo.value) == null ? void 0 : $.base_url), 1)])), e("tr", null, [e("td", null, t(a.$t("settings.server_as_addon")), 1), e("td", null, [l(D, {
+                                icon: (w = i(s).serverInfo.value) != null && w.homeassistant_addon ? "mdi-check" : "mdi-close"
+                            }, null, 8, ["icon"])])]), e("tr", null, [e("td", null, t(a.$t("settings.artists_in_library")), 1), e("td", null, t(f.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.albums_in_library")), 1), e("td", null, t(_.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.tracks_in_library")), 1), e("td", null, t(m.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.playlists_in_library")), 1), e("td", null, t(v.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.radio_in_library")), 1), e("td", null, t(c.value), 1)]), e("tr", null, [e("td", null, t(a.$t("settings.server_logging")), 1), e("td", null, [e("a", {
+                                href: `${i(s).baseUrl}/log`,
+                                target: "_blank"
+                            }, t(a.$t("settings.download_log")), 9, ie)])])])]
                         }),
                         _: 1
                     })]),
                     _: 1
                 })])], 64)
             }
         }
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/CoreConfigs-fc1a0848.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/CoreConfigs-fc1a0848.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Default-7a0e81ad.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Default-e0bfb99e.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -72,30 +72,30 @@
     ag as nl,
     ah as sl,
     ai as rl,
     aj as at,
     ak as ul,
     al as cl,
     am as dl
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     V as it,
     a as vl,
     b as nt
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     u as Pe,
     a as ml,
     V as ae,
     b as me,
     c as gt,
     m as pl,
     d as fl,
     e as yl
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     m as He,
     a as re,
     b as qe,
     c as Ae,
     d as be,
     u as Fe,
@@ -115,77 +115,77 @@
     q as kt,
     r as wl,
     s as Vl,
     v as $l,
     M as Pl,
     w as xl,
     x as Sl
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     m as Ue,
     u as Qe,
     a as Il,
     b as Bl,
     c as Tl
-} from "./layout-087be267.js";
+} from "./layout-2c008654.js";
 import {
     _ as Xe,
     i as Ml,
     a as El,
     b as zl,
     c as Rl,
     g as st
-} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
+} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
 import {
     L as Z,
     _ as rt,
     a as xe,
     B as X
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     e as we
 } from "./eventbus-d154090d.js";
 import {
     V as je,
     a as Ct
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     V as ze,
     a as Se,
     b as Nl,
     c as Ll
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     V as Ge
-} from "./VDialog-ccbfddc9.js";
+} from "./VDialog-b35e6970.js";
 import {
     V as Wl
-} from "./VTextField-f81f9175.js";
+} from "./VTextField-be284f64.js";
 import {
     g as Dl,
     a as Hl
-} from "./contextmenu-ec34ccac.js";
+} from "./contextmenu-7e32a8e5.js";
 import {
     V as ql,
     a as wt,
     b as Al,
     c as Fl,
     d as Ol,
     e as Yl
-} from "./VExpansionPanel-286d9c63.js";
+} from "./VExpansionPanel-523a6df6.js";
 import {
     V as Vt
-} from "./VBadge-8be61727.js";
+} from "./VBadge-8b6f3afa.js";
 import {
     C as Ul
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     V as Ql
-} from "./VCheckboxBtn-d54a899d.js";
-import "./index-0afee102.js"; /* empty css              */
+} from "./VCheckboxBtn-4c08e900.js";
+import "./index-a4f9d82d.js"; /* empty css              */
 function Xl(e) {
     let {
         rootEl: t,
         isSticky: a,
         layoutItemStyles: i
     } = e;
     const l = K(!1),
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Default-872711e9.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Default-872711e9.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditConfig-0f6f6afc.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditConfig-0f6f6afc.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditConfig.vue_vue_type_style_index_0_lang-74792501.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -20,59 +20,59 @@
     F as Q,
     B as W,
     N as w,
     J as h,
     D as L,
     q as p,
     I as V
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     b as ne,
     c as re,
     d as ve,
     e as me,
     a as pe,
     V as ce
-} from "./VExpansionPanel-286d9c63.js";
+} from "./VExpansionPanel-523a6df6.js";
 import {
     a as be,
     i as le,
     L as Ve,
     N as ke,
     x as ge,
     V as T
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     e as he,
     f as Ce,
     m as fe,
     g as $e,
     u as Ee,
     c as X,
     h as Y,
     i as Z
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     g as we,
     b as Se
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     a as Ue,
     V as qe,
     d as Pe
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     V as Re
-} from "./VSpacer-4e341220.js";
+} from "./VSpacer-b8926de0.js";
 import {
     V as Ie
-} from "./VDialog-ccbfddc9.js";
+} from "./VDialog-b35e6970.js";
 import {
     V as D
-} from "./VTextField-f81f9175.js";
+} from "./VTextField-be284f64.js";
 const Te = _({
         ...be(),
         ...he()
     }, "VForm"),
     Ae = ee()({
         name: "VForm",
         props: Te(),
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditCoreConfig-e48660bd.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditCoreConfig-b660ec39.js`

 * *Files 5% similar despite different names*

#### js-beautify {}

```diff
@@ -10,40 +10,40 @@
     N as m,
     J as u,
     q as d,
     x as p,
     I as r,
     D as f,
     H as n
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as $
-} from "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js";
+} from "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js";
 import {
     n as B
 } from "./index.browser-7e542916.js";
 import {
     c as D,
     b as v,
     V as E
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     b as h,
     e as O
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     x as S
-} from "./VBtn-a0da5efe.js";
-import "./VExpansionPanel-286d9c63.js";
-import "./VTextField-f81f9175.js";
-import "./index-0afee102.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VListItem-943ee224.js";
-import "./VSpacer-4e341220.js";
-import "./VDialog-ccbfddc9.js";
+} from "./VBtn-49774b84.js";
+import "./VExpansionPanel-523a6df6.js";
+import "./VTextField-be284f64.js";
+import "./index-a4f9d82d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VListItem-b049d12d.js";
+import "./VSpacer-b8926de0.js";
+import "./VDialog-b35e6970.js";
 const T = {
         key: 0,
         style: {
             "margin-left": "-5px",
             "margin-right": "-5px"
         }
     },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditPlayer-9b8c67de.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditPlayer-7719345f.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -10,37 +10,37 @@
     q as t,
     N as d,
     J as r,
     I as n,
     D as u,
     x as p,
     H as l
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     V as N,
     _ as B
-} from "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js";
+} from "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js";
 import {
     c as I,
     b as m,
     V as S
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     b as g
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as T
-} from "./VTextField-f81f9175.js";
-import "./VExpansionPanel-286d9c63.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./index-0afee102.js";
-import "./VBtn-a0da5efe.js";
-import "./VListItem-943ee224.js";
-import "./VSpacer-4e341220.js";
-import "./VDialog-ccbfddc9.js";
+} from "./VTextField-be284f64.js";
+import "./VExpansionPanel-523a6df6.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./index-a4f9d82d.js";
+import "./VBtn-49774b84.js";
+import "./VListItem-b049d12d.js";
+import "./VSpacer-b8926de0.js";
+import "./VDialog-b35e6970.js";
 const D = {
         key: 0,
         style: {
             "margin-left": "-5px",
             "margin-right": "-5px"
         }
     },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/EditProvider-f7b6707b.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/EditProvider-7ffddf94.js`

 * *Files 10% similar despite different names*

#### js-beautify {}

```diff
@@ -13,43 +13,43 @@
     y as d,
     q as i,
     N as p,
     J as m,
     x as f,
     I as u,
     D as v
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     V as E,
     _ as I
-} from "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js";
+} from "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js";
 import {
     n as P
 } from "./index.browser-7e542916.js";
 import {
     c as U,
     b as _,
     V as O
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     b as h,
     e as A
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as D
-} from "./VTextField-f81f9175.js";
+} from "./VTextField-be284f64.js";
 import {
     x as H
-} from "./VBtn-a0da5efe.js";
-import "./VExpansionPanel-286d9c63.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VSpacer-4e341220.js";
-import "./VDialog-ccbfddc9.js";
+} from "./VBtn-49774b84.js";
+import "./VExpansionPanel-523a6df6.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VSpacer-b8926de0.js";
+import "./VDialog-b35e6970.js";
 const q = {
         key: 0,
         style: {
             "margin-left": "-5px",
             "margin-right": "-5px"
         }
     },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/HomeView-297a9bbc.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/HomeView-eae672c0.js`

 * *Files 10% similar despite different names*

#### js-beautify {}

```diff
@@ -1,34 +1,34 @@
 import {
     V as r,
     a as m
-} from "./VRow-73379099.js";
+} from "./VRow-08fca7f1.js";
 import {
     a as c
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     V as p
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     V as d,
     j as u
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     l as _,
     r as f,
     v as i,
     A as o,
     I as l,
     j as a,
     y as t,
     F as h,
     B as b,
     x as g,
     J as V
-} from "./index-dcf0de03.js"; /* empty css              */
+} from "./index-8ef8125d.js"; /* empty css              */
 const v = {
         style: {
             "margin-left": "10px",
             "margin-right": "10px",
             "margin-top": "10px",
             "margin-bottom": "10px"
         }
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ItemsListing-9c236e22.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ItemsListing-9c236e22.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -1,11 +1,11 @@
 import {
     L as Ve,
     s as Ie
-} from "./ListviewItem-2c46c8ee.js"; /* empty css                             */
+} from "./ListviewItem-ade956db.js"; /* empty css                             */
 import {
     p as Ae,
     m as Fe,
     ay as Me,
     g as Ne,
     f as Le,
     d as Pe,
@@ -34,45 +34,45 @@
     E as B,
     N as q,
     q as E,
     F as G,
     B as J,
     G as k,
     X as He
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     B as O,
     _ as ne,
     L as X
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     _ as qe
-} from "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
+} from "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
 import {
     i as je,
     a as Ue
-} from "./contextmenu-ec34ccac.js";
+} from "./contextmenu-7e32a8e5.js";
 import {
     A as se
-} from "./Alert-eb81bdeb.js";
+} from "./Alert-bdc4de4a.js";
 import {
     C as Ge
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     e as Je
 } from "./eventbus-d154090d.js";
 import {
     V as We
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     V as Xe
-} from "./VTextField-f81f9175.js";
+} from "./VTextField-be284f64.js";
 import {
     V as re
-} from "./VBadge-8be61727.js";
+} from "./VBadge-8b6f3afa.js";
 import {
     y as Ze,
     z as Qe,
     c as Ye,
     A as xe,
     B as et,
     C as tt,
@@ -80,34 +80,34 @@
     g as at,
     i as lt,
     E as it,
     F as nt,
     j as L,
     k as st,
     V as ue
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     a as de
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     f as rt,
     a as ut,
     e as ce,
     g as dt,
     V as Z,
     c as Q,
     b as Y
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as ct,
     a as vt
-} from "./VRow-73379099.js";
+} from "./VRow-08fca7f1.js";
 import {
     b as ft
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 const mt = Ae({
         multiLine: Boolean,
         timeout: {
             type: [Number, String],
             default: 5e3
         },
         vertical: Boolean,
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxEIzIFKw-8007dfe8.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxEIzIFKw-8007dfe8.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxFIzIFKw-8e48cf20.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxFIzIFKw-8e48cf20.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxGIzIFKw-10b31f4c.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxGIzIFKw-10b31f4c.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxHIzIFKw-ca7eea0c.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxHIzIFKw-ca7eea0c.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxIIzI-0f303f31.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxIIzI-0f303f31.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxLIzIFKw-8c3798e3.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxLIzIFKw-8c3798e3.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxMIzIFKw-638764dc.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxMIzIFKw-638764dc.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fABc4EsA-3728fbdd.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fABc4EsA-3728fbdd.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBBc4-b0195382.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBBc4-b0195382.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBxc4EsA-713780d8.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fBxc4EsA-713780d8.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCBc4EsA-ef8f0236.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCBc4EsA-ef8f0236.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCRc4EsA-aeed0e51.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCRc4EsA-aeed0e51.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fChc4EsA-7f1c829b.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fChc4EsA-7f1c829b.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCxc4EsA-0948409a.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmEU9fCxc4EsA-0948409a.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fABc4EsA-47aa3bfa.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fABc4EsA-47aa3bfa.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBBc4-f7591131.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBBc4-f7591131.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBxc4EsA-455c2c1a.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fBxc4EsA-455c2c1a.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCBc4EsA-20dc200c.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCBc4EsA-20dc200c.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCRc4EsA-435e4b7f.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCRc4EsA-435e4b7f.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fChc4EsA-b076e863.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fChc4EsA-b076e863.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCxc4EsA-51f3f418.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmSU5fCxc4EsA-51f3f418.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfABc4EsA-6a84eeee.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfABc4EsA-6a84eeee.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBBc4-f5aebdfe.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBBc4-f5aebdfe.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBxc4EsA-1c9cc76f.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfBxc4EsA-1c9cc76f.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCBc4EsA-5b6377da.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCBc4EsA-5b6377da.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCRc4EsA-3c505383.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCRc4EsA-3c505383.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfChc4EsA-fc66f942.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfChc4EsA-fc66f942.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCxc4EsA-4ec57f2a.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmWUlfCxc4EsA-4ec57f2a.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfABc4EsA-9fdb12ce.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfABc4EsA-9fdb12ce.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBBc4-7e262106.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBBc4-7e262106.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBxc4EsA-2550c2e2.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfBxc4EsA-2550c2e2.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCBc4EsA-76da333a.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCBc4EsA-76da333a.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCRc4EsA-f265cee6.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCRc4EsA-f265cee6.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfChc4EsA-2781e9e7.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfChc4EsA-2781e9e7.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCxc4EsA-3a38c967.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOlCnqEu92Fr1MmYUtfCxc4EsA-3a38c967.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4WxKOzY-daf51ab5.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4WxKOzY-daf51ab5.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4mxK-f6734f81.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4mxK-f6734f81.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu5mxKOzY-495d38d4.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu5mxKOzY-495d38d4.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu72xKOzY-b7ef2cd1.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu72xKOzY-b7ef2cd1.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7GxKOzY-3c23eb02.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7GxKOzY-3c23eb02.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7WxKOzY-77b24796.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7WxKOzY-77b24796.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7mxKOzY-d368cf5b.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7mxKOzY-d368cf5b.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryAlbums-e581ef5e.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryAlbums-cc4c5558.js`

 * *Files 9% similar despite different names*

#### js-beautify {}

```diff
@@ -1,40 +1,40 @@
 import {
     _ as u
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     l as c,
     r as l,
     o as f,
     H as e,
     ao as o,
     b as _,
     v as d,
     x as b,
     M as m,
     ap as r
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
 const W = c({
     __name: "LibraryAlbums",
     setup(y) {
         const n = l([]),
             i = l(!1);
         f(() => {
             const t = e.subscribe_multi([o.MEDIA_ITEM_ADDED, o.MEDIA_ITEM_UPDATED, o.MEDIA_ITEM_DELETED], a => {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryArtists-b9bf1b9d.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryArtists-be2722d0.js`

 * *Files 11% similar despite different names*

#### js-beautify {}

```diff
@@ -1,40 +1,40 @@
 import {
     _ as u
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     l as f,
     r as l,
     o as c,
     H as e,
     ao as r,
     b as _,
     v as y,
     x as d,
     M as n,
     ap as o
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
 const P = f({
     __name: "LibraryArtists",
     setup(v) {
         const p = l([]),
             a = l(!1),
             m = async function(t) {
                 if (t.refresh) {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryPlaylists-b4797965.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryPlaylists-14676281.js`

 * *Files 14% similar despite different names*

#### js-beautify {}

```diff
@@ -7,36 +7,36 @@
     P as v,
     ao as r,
     b,
     v as h,
     x as E,
     M as p,
     ap as l
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as w
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
 const z = y({
     __name: "LibraryPlaylists",
     setup(T) {
         const {
             t: m
         } = _(), u = o([]), s = o(!1), n = o([]), c = async function(t) {
             if (t.refresh) {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/LibraryRadios-31300560.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/LibraryTracks-ecb94887.js`

 * *Files 11% similar despite different names*

#### js-beautify {}

```diff
@@ -1,87 +1,88 @@
 import {
-    l as d,
-    L as f,
+    l as f,
+    L as d,
     r as m,
     o as _,
     H as a,
-    ao as i,
+    ao as s,
     b as y,
     v as b,
-    x as h,
-    M as s,
+    x as v,
+    M as i,
     ap as n
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
-    _ as v
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+    _ as h
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
-const z = d({
-    __name: "LibraryRadios",
-    setup(D) {
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
+const q = f({
+    __name: "LibraryTracks",
+    setup(k) {
         const {
             t: l
-        } = f(), u = m([]), o = m(!1);
+        } = d(), u = m([]), r = m(!1);
         _(() => {
-            const t = a.subscribe_multi([i.MEDIA_ITEM_ADDED, i.MEDIA_ITEM_UPDATED, i.MEDIA_ITEM_DELETED], e => {
-                var r;
-                (r = e.object_id) != null && r.startsWith("library://radio") && (o.value = !0)
+            const t = a.subscribe_multi([s.MEDIA_ITEM_ADDED, s.MEDIA_ITEM_UPDATED, s.MEDIA_ITEM_DELETED], e => {
+                var o;
+                (o = e.object_id) != null && o.startsWith("library://track") && (r.value = !0)
             });
             y(t)
         });
-        const p = async function(t) {
-            if (t.refresh) {
-                for (a.startSync([s.RADIO]), await n(250); a.syncTasks.value.length > 0 && a.syncTasks.value.filter(e => e.media_types.includes(s.RADIO)).length != 0;) await n(500);
+        const c = async function(t) {
+            if (t.favoritesOnly = t.favoritesOnly || void 0, t.refresh) {
+                for (a.startSync([i.TRACK]), await n(250); a.syncTasks.value.length > 0 && a.syncTasks.value.filter(e => e.media_types.includes(i.TRACK)).length != 0;) await n(500);
                 await n(500)
             }
-            return o.value = !1, await a.getLibraryRadios(t.favoritesOnly || void 0, t.search, t.limit, t.offset, t.sortBy)
-        }, c = async function() {
+            return r.value = !1, await a.getLibraryTracks(t.favoritesOnly, t.search, t.limit, t.offset, t.sortBy)
+        }, p = async function() {
             const t = prompt(l("enter_url"));
-            t && a.getItem(s.RADIO, t, "url").then(e => {
-                const r = prompt(l("enter_name"), e.name);
-                e.name = r || e.name, a.addItemToLibrary(e).then(() => o.value = !0)
+            t && a.getItem(i.TRACK, t, "url").then(e => {
+                const o = prompt(l("enter_name"), e.name);
+                e.name = o || e.name, a.addItemToLibrary(e).then(() => r.value = !0)
             }).catch(e => alert(e))
         };
-        return (t, e) => (b(), h(v, {
-            itemtype: "radios",
+        return (t, e) => (b(), v(h, {
+            itemtype: "tracks",
             items: u.value,
-            "show-duration": !1,
             "show-provider": !1,
             "show-favorites-only-filter": !0,
-            "load-data": p,
-            "sort-keys": ["sort_name", "timestamp_added DESC"],
-            "update-available": o.value,
-            title: t.$t("radios"),
+            "show-track-number": !1,
+            "load-data": c,
+            "sort-keys": ["sort_name", "timestamp_added DESC", "sort_artist", "duration"],
+            "show-album": !1,
+            "update-available": r.value,
+            title: t.$t("tracks"),
             "show-search-button": !0,
             "allow-key-hooks": !0,
             "context-menu-items": [{
                 label: "add_url_item",
                 labelArgs: [],
                 action: () => {
-                    c()
+                    p()
                 },
                 icon: "mdi-link-plus"
             }]
         }, null, 8, ["items", "update-available", "title", "context-menu-items"]))
     }
 });
 export {
-    z as
+    q as
     default
 };
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListItem-3da12b03.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListItem-3da12b03.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListItem-6dad7331.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListItem-bba986fb.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -13,27 +13,27 @@
     y as l,
     Z as b,
     k as M,
     Q as g,
     j as f,
     F as B,
     D as w
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     j as $,
     V as P
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     c as A,
     V as C
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     b as x,
     V as H
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 const T = ["title", "innerHTML"],
     D = ["title", "innerHTML"],
     Z = L({
         __name: "ProviderIcon",
         props: {
             domain: {},
             size: {},
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListviewItem-2c46c8ee.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListviewItem-ade956db.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -43,50 +43,50 @@
     M as P,
     H as me,
     an as Xe,
     ar as Je,
     ab as X,
     G as ee,
     U as Qe
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as Ze,
     d as xe
-} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
+} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
 import {
     _ as et,
     B as tt,
     L as it,
     a as st
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     m as rt,
     b as ot,
     u as nt,
     c as fe,
     d as he
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     i as Ve,
     a as lt,
     o as at,
     d as ut,
     q as dt,
     s as ct,
     v as mt,
     j,
     V as ft,
     l as ht
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     f as pt,
     a as vt,
     e as pe,
     g as yt
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 const bt = le({
         ...rt(),
         ...Se(ot(), ["inline"])
     }, "VCheckbox"),
     gt = Z()({
         name: "VCheckbox",
         inheritAttrs: !1,
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ListviewItem-54a3402d.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ListviewItem-54a3402d.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-11ec382a.woff` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-11ec382a.woff`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-29c11fa5.ttf` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-29c11fa5.ttf`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-5743ed3d.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-5743ed3d.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MaterialIcons-Regular-e69d687a.eot` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MaterialIcons-Regular-e69d687a.eot`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MediaItemThumb-5ee47663.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MediaItemThumb-5ee47663.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -16,37 +16,37 @@
     Y as p,
     A as w,
     aD as m,
     r as C,
     ac as y,
     w as H,
     aj as v
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as O
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     V as M
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     V as Y,
     b as N,
     c as E
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as S,
     c as X
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     a as U
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     x as L,
     l as P
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 const T = "" + new URL("crossfade-ba51f69a.png", import.meta.url).href,
     Z = "data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACQAAAAkCAYAAADhAJiYAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAABmJLR0QAAAAAAAD5Q7t/AAAACXBIWXMAAABgAAAAYADwa0LPAAAAnElEQVRYw+2UwQ6AMAhDwfjh+OXzZrgslqxjW8K7GWdtRqlIUYyh/qG1Zt8LVYuKzTDUnCGNy41zrfhpGRrhZgn5/HmiWdzuhsrQH7QMicjDENmuGKEbQjaotiwLaGSZeUIzZB2jhnwfAdqyzFAze+gXxPSZxcgaB6JDa+rUDLG2DNFJ3TLkzDlN3bveGWc83ZFlctTIKOVWFCt5AYSDaENMYFhMAAAAJXRFWHRkYXRlOmNyZWF0ZQAyMDIyLTA0LTE1VDEzOjExOjE0KzAwOjAwADepDgAAACV0RVh0ZGF0ZTptb2RpZnkAMjAyMi0wNC0xNVQxMzoxMToxNCswMDowMHFqEbIAAAAASUVORK5CYII=",
     x = {
         class: "d-flex justify-center",
         style: {
             width: "100%"
         }
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js`

 * *Files 3% similar despite different names*

#### js-beautify {}

```diff
@@ -13,42 +13,42 @@
     N as n,
     J as r,
     q as f,
     ab as S,
     ar as D,
     X as N,
     z as T
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as B,
     d as _
-} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
+} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
 import {
     L
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     e as z
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     a as A,
     b as F,
     c as p,
     V as H
-} from "./ListviewItem-2c46c8ee.js";
+} from "./ListviewItem-ade956db.js";
 import {
     c as M,
     a as b
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     j as c,
     l as R
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     a as j
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 const K = C({
     __name: "PanelviewItem",
     props: {
         item: {},
         size: {
             default: 200
         },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PlayerQueue-41b4928f.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PlayerQueue-8c871ec2.js`

 * *Files 3% similar despite different names*

#### js-beautify {}

```diff
@@ -23,62 +23,62 @@
     F as ie,
     B as se,
     I as w,
     z as M,
     G as L,
     a3 as re,
     M as de
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     L as me,
     s as pe
-} from "./ListviewItem-2c46c8ee.js"; /* empty css                             */
+} from "./ListviewItem-ade956db.js"; /* empty css                             */
 import {
     B as ve,
     L as c
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     C as fe
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     A as J
-} from "./Alert-eb81bdeb.js";
+} from "./Alert-bdc4de4a.js";
 import {
     V as N
-} from "./VBadge-8be61727.js";
+} from "./VBadge-8b6f3afa.js";
 import {
     V as K,
     a as _e
-} from "./VTabs-7c03bdc8.js";
+} from "./VTabs-1b99b0fa.js";
 import {
     j as g,
     V as T
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     V as O,
     c as ce,
     b as k
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as W,
     a as X
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     a as ge,
     V as be
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     b
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     V as ye
-} from "./VDialog-ccbfddc9.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./index-0afee102.js"; /* empty css              */
+} from "./VDialog-b35e6970.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./index-a4f9d82d.js"; /* empty css              */
 const qe = w("br", null, null, -1),
     Ce = {
         key: 0
     },
     Fe = ee({
         __name: "PlayerQueue",
         setup(ke) {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Players-525b85bc.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Players-2ae3919d.js`

 * *Files 4% similar despite different names*

#### js-beautify {}

```diff
@@ -16,35 +16,35 @@
     F,
     B as G,
     R as M,
     x as m,
     q as c,
     I as f,
     D as R
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     L as j,
     _ as U,
     B as g
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     C as v
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     V as q,
     j as h
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     V as z
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     b as H
-} from "./VMenu-3bdd1b96.js";
-import "./VListItem-943ee224.js"; /* empty css              */
-import "./index-0afee102.js";
+} from "./VMenu-a805d6b6.js";
+import "./VListItem-b049d12d.js"; /* empty css              */
+import "./index-a4f9d82d.js";
 const J = {
         style: {
             "margin-bottom": "10px"
         }
     },
     O = {
         class: "line-clamp-1"
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/PlaylistDetails-cce72360.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/PlaylistDetails-971d8698.js`

 * *Files 14% similar despite different names*

#### js-beautify {}

```diff
@@ -1,50 +1,50 @@
 import {
     _ as v,
     f as _
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     _ as y,
     a as k
-} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js";
+} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js";
 import {
     l as b,
     r as p,
     w as h,
     o as w,
     H as s,
     ao as D,
     b as I,
     v as l,
     A as E,
     j as T,
     x as n,
     D as u,
     ap as A
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
-import "./layout-087be267.js";
-import "./VDialog-ccbfddc9.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
+import "./layout-2c008654.js";
+import "./VDialog-b35e6970.js";
 const Y = b({
     __name: "PlaylistDetails",
     props: {
         itemId: {},
         provider: {}
     },
     setup(c) {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ProviderDetails-da7f4c54.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ProviderDetails-da7f4c54.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -25,73 +25,73 @@
     aj as N,
     M as R,
     ar as ee,
     E as te,
     H,
     X as ie,
     G as ae
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     B as oe,
     _ as K,
     L as Y
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     _ as U,
     g as j,
     d as re
-} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
+} from "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
 import {
     a as se
-} from "./contextmenu-ec34ccac.js";
+} from "./contextmenu-7e32a8e5.js";
 import {
     e as le
 } from "./eventbus-d154090d.js";
 import {
     a as ne,
     i as me,
     l as q,
     j as k,
     V as D,
     k as de
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     b as S
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     c as ue,
     b as _,
     a as E,
     V as pe,
     d as ce
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     V as fe
-} from "./ListviewItem-2c46c8ee.js";
+} from "./ListviewItem-ade956db.js";
 import {
     c as ye,
     V as x,
     b as ge
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     b as ve,
     c as be
-} from "./layout-087be267.js";
+} from "./layout-2c008654.js";
 import {
     V as he
-} from "./VDialog-ccbfddc9.js";
+} from "./VDialog-b35e6970.js";
 import {
     V as ke
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     C as _e
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     V as Ve
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 const Ce = W({
         ...ne(),
         ...ve()
     }, "VLayout"),
     $e = X()({
         name: "VLayout",
         props: Ce(),
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Providers-3598c1f3.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Providers-453e3025.js`

 * *Files 3% similar despite different names*

#### js-beautify {}

```diff
@@ -23,43 +23,43 @@
     k as Q,
     D as f,
     aS as v,
     I as y,
     R as T,
     a9 as W,
     aa as X
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     L as I,
     _ as S,
     B as b,
     a as Y
-} from "./ListItem-6dad7331.js";
+} from "./ListItem-bba986fb.js";
 import {
     A as Z
-} from "./Alert-eb81bdeb.js";
+} from "./Alert-bdc4de4a.js";
 import {
     C as x
-} from "./Container-d623752d.js";
+} from "./Container-32d4da6e.js";
 import {
     c as ee,
     b as te
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as ne,
     j as g
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     a as ae
-} from "./VCard-111cabcf.js";
+} from "./VCard-e81591ba.js";
 import {
     V as ie
-} from "./VToolbar-dfba6de4.js";
-import "./VListItem-943ee224.js"; /* empty css              */
-import "./index-0afee102.js";
+} from "./VToolbar-b4c95f12.js";
+import "./VListItem-b049d12d.js"; /* empty css              */
+import "./index-a4f9d82d.js";
 const se = p => (W("data-v-753093ab"), p = p(), X(), p),
     oe = se(() => y("br", null, null, -1)),
     re = {
         class: "line-clamp-1"
     },
     de = {
         class: "line-clamp-1"
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/RadioDetails-993d50b0.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/RadioDetails-6761105c.js`

 * *Files 13% similar despite different names*

#### js-beautify {}

```diff
@@ -1,48 +1,48 @@
 import {
     _ as u,
     f
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     _ as v,
     a as _
-} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js";
+} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js";
 import {
     l as h,
     r as w,
     w as y,
     v as a,
     A as V,
     j as k,
     x as m,
     D as n,
     I,
     H as s,
     aq as g
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
-import "./layout-087be267.js";
-import "./VDialog-ccbfddc9.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
+import "./layout-2c008654.js";
+import "./VDialog-b35e6970.js";
 const R = I("br", null, null, -1),
     W = h({
         __name: "RadioDetails",
         props: {
             itemId: {},
             provider: {}
         },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Search-433484bb.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Search-93fe9303.js`

 * *Files 7% similar despite different names*

#### js-beautify {}

```diff
@@ -1,12 +1,12 @@
 import {
     L as j,
     V as q,
     s as A
-} from "./ListviewItem-2c46c8ee.js"; /* empty css                             */
+} from "./ListviewItem-ade956db.js"; /* empty css                             */
 import {
     l as G,
     a6 as J,
     e as X,
     r as n,
     c as w,
     w as M,
@@ -24,50 +24,50 @@
     x as y,
     D as k,
     q as Q,
     k as W,
     E as Y,
     H as Z,
     X as z
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     _ as ee
-} from "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
+} from "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
 import {
     e as S
 } from "./eventbus-d154090d.js";
 import {
     V as T
-} from "./VToolbar-dfba6de4.js";
+} from "./VToolbar-b4c95f12.js";
 import {
     b as te
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     V as ae
-} from "./VTextField-f81f9175.js";
+} from "./VTextField-be284f64.js";
 import {
     a as le,
     V as se
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     V as re,
     a as oe
-} from "./VRow-73379099.js";
+} from "./VRow-08fca7f1.js";
 import {
     V as ie
-} from "./VSpacer-4e341220.js";
+} from "./VSpacer-b8926de0.js";
 import {
     V as ue,
     k as ne
-} from "./VBtn-a0da5efe.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VListItem-943ee224.js";
-import "./VCard-111cabcf.js";
-import "./index-0afee102.js"; /* empty css              */
+} from "./VBtn-49774b84.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VListItem-b049d12d.js";
+import "./VCard-e81591ba.js";
+import "./index-a4f9d82d.js"; /* empty css              */
 const ve = {
         key: 2
     },
     me = {
         style: {
             "margin-left": "15px"
         }
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/Settings-70d67eb6.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/Settings-ef547e38.js`

 * *Files 4% similar despite different names*

#### js-beautify {}

```diff
@@ -7,24 +7,24 @@
     A as _,
     j as t,
     y as r,
     N as o,
     J as s,
     x as g,
     S as y
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     a as V,
     V as n
-} from "./VTabs-7c03bdc8.js";
+} from "./VTabs-1b99b0fa.js";
 import {
     V as b
-} from "./VToolbar-dfba6de4.js";
-import "./VBtn-a0da5efe.js";
-import "./index-0afee102.js";
+} from "./VToolbar-b4c95f12.js";
+import "./VBtn-49774b84.js";
+import "./index-a4f9d82d.js";
 const x = m({
     __name: "Settings",
     setup(S) {
         const l = d(),
             u = v(() => {
                 var e, a;
                 return (e = l.currentRoute.value.name) != null && e.toString().includes("player") ? "players" : (a = l.currentRoute.value.name) != null && a.toString().includes("core") ? "core" : "providers"
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/TrackDetails-95dc4644.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/TrackDetails-807370a0.js`

 * *Files 13% similar despite different names*

#### js-beautify {}

```diff
@@ -1,15 +1,15 @@
 import {
     _ as v,
     f
-} from "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js";
+} from "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js";
 import {
     _ as g,
     a as I
-} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js";
+} from "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js";
 import {
     l as T,
     r as u,
     c as V,
     aq as m,
     w as D,
     o as A,
@@ -18,35 +18,35 @@
     b as B,
     v as n,
     A as E,
     j as $,
     x as c,
     D as d,
     I as b
-} from "./index-dcf0de03.js";
-import "./ListviewItem-2c46c8ee.js";
-import "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js";
-import "./ListItem-6dad7331.js";
-import "./VBtn-a0da5efe.js";
-import "./VMenu-3bdd1b96.js";
-import "./index-0afee102.js";
-import "./VListItem-943ee224.js";
-import "./VCheckboxBtn-d54a899d.js";
-import "./VCard-111cabcf.js"; /* empty css                             */
-import "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js";
-import "./contextmenu-ec34ccac.js";
+} from "./index-8ef8125d.js";
+import "./ListviewItem-ade956db.js";
+import "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js";
+import "./ListItem-bba986fb.js";
+import "./VBtn-49774b84.js";
+import "./VMenu-a805d6b6.js";
+import "./index-a4f9d82d.js";
+import "./VListItem-b049d12d.js";
+import "./VCheckboxBtn-4c08e900.js";
+import "./VCard-e81591ba.js"; /* empty css                             */
+import "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js";
+import "./contextmenu-7e32a8e5.js";
 import "./eventbus-d154090d.js";
-import "./Alert-eb81bdeb.js";
-import "./Container-d623752d.js"; /* empty css              */
-import "./VToolbar-dfba6de4.js";
-import "./VTextField-f81f9175.js";
-import "./VBadge-8be61727.js";
-import "./VRow-73379099.js";
-import "./layout-087be267.js";
-import "./VDialog-ccbfddc9.js";
+import "./Alert-bdc4de4a.js";
+import "./Container-32d4da6e.js"; /* empty css              */
+import "./VToolbar-b4c95f12.js";
+import "./VTextField-be284f64.js";
+import "./VBadge-8b6f3afa.js";
+import "./VRow-08fca7f1.js";
+import "./layout-2c008654.js";
+import "./VDialog-b35e6970.js";
 const F = b("br", null, null, -1),
     N = b("br", null, null, -1),
     oe = T({
         __name: "TrackDetails",
         props: {
             itemId: {},
             provider: {},
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBadge-4ff04865.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBadge-4ff04865.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBadge-8be61727.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBadge-8b6f3afa.js`

 * *Files 6% similar despite different names*

#### js-beautify {}

```diff
@@ -7,29 +7,29 @@
     ad as P,
     ac as x,
     aI as T,
     j as t,
     R,
     ah as _,
     k as u
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     a as w,
     y as I,
     c as L,
     d as $,
     G as j,
     e as A,
     g as H,
     H as M,
     B as X,
     i as Y,
     M as D,
     j as F
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 const G = S({
         bordered: Boolean,
         color: String,
         content: [Number, String],
         dot: Boolean,
         floating: Boolean,
         icon: V,
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBtn-a0da5efe.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBtn-49774b84.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -49,15 +49,15 @@
     ag as xt,
     aw as It,
     o as Vt,
     a_ as Bt,
     a$ as Pt,
     ax as $t,
     aW as Et
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 const He = ["top", "bottom"],
     Tt = ["start", "end", "left", "right"];
 
 function Rt(e, t) {
     let [a, n] = e.split(" ");
     return n || (n = K(He, a) ? "start" : K(Tt, a) ? "top" : "center"), {
         side: xe(a, t),
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VBtn-fccecd75.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VBtn-fccecd75.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCard-111cabcf.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCard-e81591ba.js`

 * *Files 5% similar despite different names*

#### js-beautify {}

```diff
@@ -23,31 +23,31 @@
     B as de,
     C as ie,
     g as se,
     U as le,
     l as ce,
     N as re,
     E as ue
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     g as b,
     i as oe,
     j as n,
     p as P,
     aH as u,
     m as ve,
     d as me,
     c as I,
     R as ge,
     af as ke
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     d as C,
     b as V
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 const ye = b()({
         name: "VCardActions",
         props: y(),
         setup(e, i) {
             let {
                 slots: t
             } = i;
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCard-790bb5b3.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCard-790bb5b3.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCheckboxBtn-d54a899d.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCheckboxBtn-4c08e900.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -31,19 +31,19 @@
     o as Ae,
     aY as le,
     n as ve,
     u as Pe,
     aZ as xe,
     aJ as Me,
     b7 as te
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     e as $e,
     d as _e
-} from "./index-0afee102.js";
+} from "./index-a4f9d82d.js";
 import {
     a as F,
     o as Fe,
     d as fe,
     A as me,
     q as De,
     i as D,
@@ -65,18 +65,18 @@
     U as qe,
     E as Ne,
     j as G,
     F as K,
     G as Ye,
     H as ge,
     M as Je
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     b as ne
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 const Ve = Symbol.for("vuetify:v-chip-group"),
     Qe = P({
         column: Boolean,
         filter: Boolean,
         valueComparator: {
             type: Function,
             default: se
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VCheckboxBtn-e9f604b5.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VCheckboxBtn-e9f604b5.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VDialog-ccbfddc9.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VDialog-b35e6970.js`

 * *Files 10% similar despite different names*

#### js-beautify {}

```diff
@@ -1,31 +1,31 @@
 import {
     f as b,
     j as y,
     a as D,
     e as f,
     g as h
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     p as S,
     g as w,
     f as x,
     r as F,
     aO as B,
     w as v,
     n as I,
     c as O,
     k as m,
     j as g,
     aP as R
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     i as T,
     F as j
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 const k = S({
         fullscreen: Boolean,
         retainFocus: {
             type: Boolean,
             default: !0
         },
         scrollable: Boolean,
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VDialog-ff1232cf.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VDialog-ff1232cf.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VExpansionPanel-286d9c63.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VExpansionPanel-523a6df6.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,11 +1,11 @@
 import {
     m as Oe,
     V as ye
-} from "./VTextField-f81f9175.js";
+} from "./VTextField-be284f64.js";
 import {
     p as U,
     g as W,
     w as me,
     j as o,
     F as Z,
     k as Q,
@@ -36,36 +36,36 @@
     R as ne,
     af as Pe,
     ah as Ce,
     b1 as Qe,
     m as Ze,
     d as el,
     i as ll
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     j as tl,
     d as al,
     V as nl,
     k as ol,
     m as sl,
     u as il,
     c as ge,
     i as ul
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     h as rl,
     i as cl,
     j as dl,
     k as vl,
     c as ml,
     V as fl,
     g as pl,
     m as Te,
     d as hl
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 import {
     a as X,
     w as _e,
     i as Y,
     J as yl,
     K as bl,
     G as gl,
@@ -79,22 +79,22 @@
     g as Le,
     e as oe,
     o as xl,
     d as Be,
     q as Vl,
     s as wl,
     v as Pl
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     V as ke
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     c as Cl,
     b as Tl
-} from "./index-0afee102.js";
+} from "./index-a4f9d82d.js";
 const _l = U({
         renderless: Boolean,
         ...X()
     }, "VVirtualScrollItem"),
     Il = W()({
         name: "VVirtualScrollItem",
         inheritAttrs: !1,
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VExpansionPanel-2b4b0a5a.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VExpansionPanel-2b4b0a5a.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VGrid-ec674b79.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VGrid-ec674b79.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VListItem-028a8916.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VListItem-028a8916.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VListItem-943ee224.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VListItem-b049d12d.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -19,15 +19,15 @@
     Q as Be,
     R as De,
     U as Ne,
     u as Re,
     K as je,
     f as _e,
     F as x
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     g as R,
     aF as Fe,
     bi as Ge,
     aG as Te,
     ag as V,
     s as P,
@@ -46,15 +46,15 @@
     j as f,
     b2 as K,
     w as xe,
     bj as He,
     R as Ke,
     af as Ue,
     F as U
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 
 function se(e) {
     let r = arguments.length > 1 && arguments[1] !== void 0 ? arguments[1] : "div",
         l = arguments.length > 2 ? arguments[2] : void 0;
     return R()({
         name: l ?? Fe(Ge(e.replace(/__/g, "-"))),
         props: {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VMenu-3bdd1b96.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VMenu-a805d6b6.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -44,34 +44,34 @@
     f as Qe,
     u as kt,
     bh as At,
     af as Vt,
     F as Lt,
     ay as Tt,
     as as Bt
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     a as Q,
     f as Ft,
     s as ge,
     g as It,
     n as et,
     b as Dt,
     B as se,
     h as Ve
-} from "./index-0afee102.js";
+} from "./index-a4f9d82d.js";
 import {
     u as Rt,
     e as Mt,
     f as _t,
     g as tt,
     V as Le,
     m as Nt,
     h as $t
-} from "./VListItem-943ee224.js";
+} from "./VListItem-b049d12d.js";
 import {
     a as ee,
     d as Oe,
     i as Z,
     F as nt,
     M as ot,
     H as at,
@@ -91,15 +91,15 @@
     X as le,
     Y as ue,
     Z as Be,
     _ as Fe,
     G as Xt,
     h as Zt,
     $ as Jt
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 const ne = new WeakMap;
 
 function Qt(e, n) {
     Object.keys(n).forEach(t => {
         if (qe(t)) {
             const o = je(t),
                 a = ne.get(e);
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VMenu-87d759b1.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VMenu-87d759b1.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VRow-73379099.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VRow-08fca7f1.js`

 * *Files 6% similar despite different names*

#### js-beautify {}

```diff
@@ -1,20 +1,20 @@
 /* empty css              */
 import {
     a as C,
     d as S
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     aE as i,
     aF as u,
     p as b,
     g as k,
     c as N,
     aG as j
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 const V = (() => i.reduce((t, a) => (t[a] = {
         type: [Boolean, String, Number],
         default: !1
     }, t), {}))(),
     v = (() => i.reduce((t, a) => {
         const e = "offset" + u(a);
         return t[e] = {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTabs-7c03bdc8.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTabs-1b99b0fa.js`

 * *Files 0% similar despite different names*

#### js-beautify {}

```diff
@@ -8,15 +8,15 @@
     j as K,
     I as de,
     H as fe,
     V as Q,
     n as me,
     p as ge,
     e as be
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     p as X,
     aH as J,
     g as Y,
     u as he,
     e as Se,
     s as z,
@@ -29,20 +29,20 @@
     ay as Te,
     r as Z,
     k as q,
     f as ke,
     t as k,
     i as ze,
     a as Ve
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     V as ee,
     a as we,
     s as Pe
-} from "./index-0afee102.js";
+} from "./index-a4f9d82d.js";
 
 function te(e) {
     const n = Math.abs(e);
     return Math.sign(e) * (n / ((1 / .501 - 2) * (1 - n) + 1))
 }
 
 function le(e) {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTabs-f9f04fad.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTabs-f9f04fad.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTextField-6adde8bb.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTextField-6adde8bb.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VTextField-f81f9175.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VTextField-be284f64.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -21,47 +21,47 @@
     aI as ye,
     f as be,
     aJ as xe,
     af as Ce,
     b4 as he,
     n as Z,
     b5 as Ve
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     d as ke,
     n as _e,
     a as Ie,
     e as Pe,
     s as Fe
-} from "./index-0afee102.js";
+} from "./index-a4f9d82d.js";
 import {
     a as Y,
     G as Se,
     i as U,
     M as Be,
     O as we,
     c as Re,
     L as Te,
     g as Le,
     e as $e,
     H as pe,
     N as Ae,
     P as De
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     i as Ee,
     k as Me,
     u as te,
     l as Ne,
     m as Oe,
     c as ee
-} from "./VCheckboxBtn-d54a899d.js";
+} from "./VCheckboxBtn-4c08e900.js";
 import {
     g as Ue
-} from "./VMenu-3bdd1b96.js";
+} from "./VMenu-a805d6b6.js";
 const je = N({
         active: Boolean,
         max: [Number, String],
         value: {
             type: [Number, String],
             default: 0
         },
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VToolbar-aa2d1d9a.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VToolbar-aa2d1d9a.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/VToolbar-dfba6de4.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/VToolbar-b4c95f12.js`

 * *Files 8% similar despite different names*

#### js-beautify {}

```diff
@@ -7,31 +7,31 @@
     c as E,
     e as D,
     u as w,
     f as F,
     g as $,
     l as j,
     F as u
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     p as V,
     g as k,
     j as a,
     m as U,
     t as q,
     d as z,
     u as A,
     s as G,
     c as h,
     i as J,
     a as o
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     b as K
-} from "./index-0afee102.js";
+} from "./index-a4f9d82d.js";
 const L = V({
         text: String,
         ...x(),
         ...y()
     }, "VToolbarTitle"),
     M = k()({
         name: "VToolbarTitle",
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/contextmenu-ec34ccac.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/contextmenu-7e32a8e5.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -1,15 +1,15 @@
 import {
     aB as r,
     M as n,
     H as o,
     a1 as t,
     aC as c,
     P as p
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 import {
     e as s
 } from "./eventbus-d154090d.js";
 const d = function(a) {
         var e;
         for (const i of a.provider_mappings)
             if (i.available && ((e = o.providers[i.provider_instance]) != null && e.available)) return !0;
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/cover_dark-75402cd0.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/cover_dark-75402cd0.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/cover_light-b832ae9e.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/cover_light-b832ae9e.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/crossfade-ba51f69a.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/crossfade-ba51f69a.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/hires-438c7046.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/hires-438c7046.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index-0afee102.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index-a4f9d82d.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -1,15 +1,15 @@
 import {
     g,
     bk as w,
     T as m,
     aG as p,
     p as S,
     bi as _
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 class u {
     constructor(r) {
         let {
             x: s,
             y: i,
             width: o,
             height: a
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index-4bf8ac1c.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index-4bf8ac1c.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/index-dcf0de03.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/index-8ef8125d.js`

 * *Files 2% similar despite different names*

#### js-beautify {}

```diff
@@ -10519,133 +10519,133 @@
 }
 
 function og() {
     return Ce(zo)
 }
 const kh = [{
         path: "/",
-        component: () => pe(() => import("./Default-7a0e81ad.js"), ["./Default-7a0e81ad.js", "./VListItem-943ee224.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VListItem-028a8916.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VMenu-87d759b1.css", "./layout-087be267.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./eventbus-d154090d.js", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./contextmenu-ec34ccac.js", "./VExpansionPanel-286d9c63.js", "./VExpansionPanel-2b4b0a5a.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./Default-872711e9.css"], import.meta.url),
+        component: () => pe(() => import("./Default-e0bfb99e.js"), ["./Default-e0bfb99e.js", "./VListItem-b049d12d.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VListItem-028a8916.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VMenu-87d759b1.css", "./layout-2c008654.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./eventbus-d154090d.js", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./contextmenu-7e32a8e5.js", "./VExpansionPanel-523a6df6.js", "./VExpansionPanel-2b4b0a5a.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./Default-872711e9.css"], import.meta.url),
         children: [{
             path: "",
             redirect: "/home",
             name: "homeredirect"
         }, {
             path: "/home",
             name: "home",
-            component: () => pe(() => import("./HomeView-297a9bbc.js"), ["./HomeView-297a9bbc.js", "./VRow-73379099.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VGrid-ec674b79.css", "./VCard-111cabcf.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VCard-790bb5b3.css", "./HomeView-f559b858.css"], import.meta.url),
+            component: () => pe(() => import("./HomeView-eae672c0.js"), ["./HomeView-eae672c0.js", "./VRow-08fca7f1.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VGrid-ec674b79.css", "./VCard-e81591ba.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VCard-790bb5b3.css", "./HomeView-f559b858.css"], import.meta.url),
             props: !0
         }, {
             path: "/search",
             name: "search",
-            component: () => pe(() => import("./Search-433484bb.js"), ["./Search-433484bb.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./eventbus-d154090d.js", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VRow-73379099.js", "./VGrid-ec674b79.css", "./VSpacer-4e341220.js", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./Search-93fe9303.js"), ["./Search-93fe9303.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./eventbus-d154090d.js", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VRow-08fca7f1.js", "./VGrid-ec674b79.css", "./VSpacer-b8926de0.js", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/browse",
             name: "browse",
-            component: () => pe(() => import("./BrowseView-c902aae4.js"), ["./BrowseView-c902aae4.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./BrowseView-dc407ea0.js"), ["./BrowseView-dc407ea0.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: e => ({
                 path: e.query.path
             })
         }, {
             path: "/artists",
             name: "artists",
-            component: () => pe(() => import("./LibraryArtists-b9bf1b9d.js"), ["./LibraryArtists-b9bf1b9d.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./LibraryArtists-be2722d0.js"), ["./LibraryArtists-be2722d0.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/tracks",
             name: "tracks",
-            component: () => pe(() => import("./LibraryTracks-676be9ae.js"), ["./LibraryTracks-676be9ae.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./LibraryTracks-ecb94887.js"), ["./LibraryTracks-ecb94887.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/albums",
             name: "albums",
-            component: () => pe(() => import("./LibraryAlbums-e581ef5e.js"), ["./LibraryAlbums-e581ef5e.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./LibraryAlbums-cc4c5558.js"), ["./LibraryAlbums-cc4c5558.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/playlists",
             name: "playlists",
-            component: () => pe(() => import("./LibraryPlaylists-b4797965.js"), ["./LibraryPlaylists-b4797965.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./LibraryPlaylists-14676281.js"), ["./LibraryPlaylists-14676281.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/radios",
             name: "radios",
-            component: () => pe(() => import("./LibraryRadios-31300560.js"), ["./LibraryRadios-31300560.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./LibraryRadios-d371d843.js"), ["./LibraryRadios-d371d843.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/artists/:provider/:itemId",
             name: "artist",
-            component: () => pe(() => import("./ArtistDetails-dcd8523b.js"), ["./ArtistDetails-dcd8523b.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js", "./layout-087be267.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
+            component: () => pe(() => import("./ArtistDetails-b3bb2766.js"), ["./ArtistDetails-b3bb2766.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js", "./layout-2c008654.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
             props: !0
         }, {
             path: "/albums/:provider/:itemId",
             name: "album",
-            component: () => pe(() => import("./AlbumDetails-8595c1ca.js"), ["./AlbumDetails-8595c1ca.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js", "./layout-087be267.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
+            component: () => pe(() => import("./AlbumDetails-28f977b9.js"), ["./AlbumDetails-28f977b9.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js", "./layout-2c008654.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
             props: !0
         }, {
             path: "/tracks/:provider/:itemId",
             name: "track",
-            component: () => pe(() => import("./TrackDetails-95dc4644.js"), ["./TrackDetails-95dc4644.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js", "./layout-087be267.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
+            component: () => pe(() => import("./TrackDetails-807370a0.js"), ["./TrackDetails-807370a0.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js", "./layout-2c008654.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
             props: e => ({
                 ...e.params,
                 ...e.query
             })
         }, {
             path: "/radios/:provider/:itemId",
             name: "radio",
-            component: () => pe(() => import("./RadioDetails-993d50b0.js"), ["./RadioDetails-993d50b0.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js", "./layout-087be267.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
+            component: () => pe(() => import("./RadioDetails-6761105c.js"), ["./RadioDetails-6761105c.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js", "./layout-2c008654.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
             props: !0
         }, {
             path: "/playlists/:provider/:itemId",
             name: "playlist",
-            component: () => pe(() => import("./PlaylistDetails-cce72360.js"), ["./PlaylistDetails-cce72360.js", "./ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-ec34ccac.js", "./eventbus-d154090d.js", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VTextField-f81f9175.js", "./VTextField-6adde8bb.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VRow-73379099.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js", "./layout-087be267.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
+            component: () => pe(() => import("./PlaylistDetails-971d8698.js"), ["./PlaylistDetails-971d8698.js", "./ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js", "./PanelviewItem-14a6b77a.css", "./contextmenu-7e32a8e5.js", "./eventbus-d154090d.js", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VTextField-be284f64.js", "./VTextField-6adde8bb.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VRow-08fca7f1.js", "./ItemsListing-9c236e22.css", "./vue-virtual-scroller-4d71315f.css", "./ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js", "./layout-2c008654.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./ProviderDetails-da7f4c54.css"], import.meta.url),
             props: !0
         }, {
             path: "/playerqueue",
             name: "playerqueue",
-            component: () => pe(() => import("./PlayerQueue-41b4928f.js"), ["./PlayerQueue-41b4928f.js", "./ListviewItem-2c46c8ee.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-d54a899d.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./VBadge-8be61727.js", "./VBadge-4ff04865.css", "./VTabs-7c03bdc8.js", "./VTabs-f9f04fad.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+            component: () => pe(() => import("./PlayerQueue-8c871ec2.js"), ["./PlayerQueue-8c871ec2.js", "./ListviewItem-ade956db.js", "./MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./VCheckboxBtn-4c08e900.js", "./VCheckboxBtn-e9f604b5.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./MediaItemThumb-5ee47663.css", "./ListviewItem-54a3402d.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./VBadge-8b6f3afa.js", "./VBadge-4ff04865.css", "./VTabs-1b99b0fa.js", "./VTabs-f9f04fad.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
             props: !0
         }, {
             path: "/settings",
             name: "settings",
-            component: () => pe(() => import("./Settings-70d67eb6.js"), ["./Settings-70d67eb6.js", "./VTabs-7c03bdc8.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./index-0afee102.js", "./VTabs-f9f04fad.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css"], import.meta.url),
+            component: () => pe(() => import("./Settings-ef547e38.js"), ["./Settings-ef547e38.js", "./VTabs-1b99b0fa.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./index-a4f9d82d.js", "./VTabs-f9f04fad.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css"], import.meta.url),
             props: !0,
             children: [{
                 path: "providers",
                 name: "providersettings",
-                component: () => pe(() => import("./Providers-3598c1f3.js"), ["./Providers-3598c1f3.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./Alert-eb81bdeb.js", "./Alert-eefd31ea.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./Providers-3820a270.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
+                component: () => pe(() => import("./Providers-453e3025.js"), ["./Providers-453e3025.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./Alert-bdc4de4a.js", "./Alert-eefd31ea.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./Providers-3820a270.css", "./vue-virtual-scroller-4d71315f.css"], import.meta.url),
                 props: !0
             }, {
                 path: "players",
                 name: "playersettings",
-                component: () => pe(() => import("./Players-525b85bc.js"), ["./Players-525b85bc.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css"], import.meta.url),
+                component: () => pe(() => import("./Players-2ae3919d.js"), ["./Players-2ae3919d.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css"], import.meta.url),
                 props: !0
             }, {
                 path: "core",
                 name: "coresettings",
-                component: () => pe(() => import("./CoreConfigs-6f585b64.js"), ["./CoreConfigs-6f585b64.js", "./ListItem-6dad7331.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VMenu-3bdd1b96.js", "./index-0afee102.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./Container-d623752d.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-dfba6de4.js", "./VToolbar-aa2d1d9a.css", "./CoreConfigs-fc1a0848.css"], import.meta.url),
+                component: () => pe(() => import("./CoreConfigs-f7edf5eb.js"), ["./CoreConfigs-f7edf5eb.js", "./ListItem-bba986fb.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VMenu-a805d6b6.js", "./index-a4f9d82d.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VMenu-87d759b1.css", "./ListItem-3da12b03.css", "./Container-32d4da6e.js", "./Container-8440890a.css", "./VGrid-ec674b79.css", "./VToolbar-b4c95f12.js", "./VToolbar-aa2d1d9a.css", "./CoreConfigs-fc1a0848.css"], import.meta.url),
                 props: !0
             }, {
                 path: "addprovider/:domain",
                 name: "addprovider",
-                component: () => pe(() => import("./AddProvider-0b5f3371.js"), ["./AddProvider-0b5f3371.js", "./index.browser-7e542916.js", "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js", "./VExpansionPanel-286d9c63.js", "./VTextField-f81f9175.js", "./index-0afee102.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-d54a899d.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-3bdd1b96.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./VSpacer-4e341220.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css"], import.meta.url),
+                component: () => pe(() => import("./AddProvider-1cb2a794.js"), ["./AddProvider-1cb2a794.js", "./index.browser-7e542916.js", "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js", "./VExpansionPanel-523a6df6.js", "./VTextField-be284f64.js", "./index-a4f9d82d.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-4c08e900.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-a805d6b6.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./VSpacer-b8926de0.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css"], import.meta.url),
                 props: !0
             }, {
                 path: "editprovider/:instanceId",
                 name: "editprovider",
-                component: () => pe(() => import("./EditProvider-f7b6707b.js"), ["./EditProvider-f7b6707b.js", "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js", "./VExpansionPanel-286d9c63.js", "./VTextField-f81f9175.js", "./index-0afee102.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-d54a899d.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-3bdd1b96.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./VSpacer-4e341220.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css", "./index.browser-7e542916.js"], import.meta.url),
+                component: () => pe(() => import("./EditProvider-7ffddf94.js"), ["./EditProvider-7ffddf94.js", "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js", "./VExpansionPanel-523a6df6.js", "./VTextField-be284f64.js", "./index-a4f9d82d.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-4c08e900.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-a805d6b6.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./VSpacer-b8926de0.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css", "./index.browser-7e542916.js"], import.meta.url),
                 props: !0
             }, {
                 path: "editplayer/:playerId",
                 name: "editplayer",
-                component: () => pe(() => import("./EditPlayer-9b8c67de.js"), ["./EditPlayer-9b8c67de.js", "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js", "./VExpansionPanel-286d9c63.js", "./VTextField-f81f9175.js", "./index-0afee102.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-d54a899d.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-3bdd1b96.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./VSpacer-4e341220.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css"], import.meta.url),
+                component: () => pe(() => import("./EditPlayer-7719345f.js"), ["./EditPlayer-7719345f.js", "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js", "./VExpansionPanel-523a6df6.js", "./VTextField-be284f64.js", "./index-a4f9d82d.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-4c08e900.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-a805d6b6.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./VSpacer-b8926de0.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css"], import.meta.url),
                 props: !0
             }, {
                 path: "editcore/:domain",
                 name: "editcore",
-                component: () => pe(() => import("./EditCoreConfig-e48660bd.js"), ["./EditCoreConfig-e48660bd.js", "./EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js", "./VExpansionPanel-286d9c63.js", "./VTextField-f81f9175.js", "./index-0afee102.js", "./VBtn-a0da5efe.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-d54a899d.js", "./VListItem-943ee224.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-3bdd1b96.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-111cabcf.js", "./VCard-790bb5b3.css", "./VSpacer-4e341220.js", "./VDialog-ccbfddc9.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css", "./index.browser-7e542916.js"], import.meta.url),
+                component: () => pe(() => import("./EditCoreConfig-b660ec39.js"), ["./EditCoreConfig-b660ec39.js", "./EditConfig.vue_vue_type_style_index_0_lang-74792501.js", "./VExpansionPanel-523a6df6.js", "./VTextField-be284f64.js", "./index-a4f9d82d.js", "./VBtn-49774b84.js", "./VBtn-fccecd75.css", "./VCheckboxBtn-4c08e900.js", "./VListItem-b049d12d.js", "./VListItem-028a8916.css", "./VCheckboxBtn-e9f604b5.css", "./VMenu-a805d6b6.js", "./VMenu-87d759b1.css", "./VTextField-6adde8bb.css", "./VExpansionPanel-2b4b0a5a.css", "./VCard-e81591ba.js", "./VCard-790bb5b3.css", "./VSpacer-b8926de0.js", "./VDialog-b35e6970.js", "./VDialog-ff1232cf.css", "./EditConfig-0f6f6afc.css", "./index.browser-7e542916.js"], import.meta.url),
                 props: !0
             }, {
                 path: "",
                 redirect: "/settings/providers",
                 name: "settingsredirect"
             }]
         }]
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/info_gradient-a4aefd1d.jpg` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/info_gradient-a4aefd1d.jpg`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/layout-087be267.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/layout-2c008654.js`

 * *Files 1% similar despite different names*

#### js-beautify {}

```diff
@@ -1,10 +1,10 @@
 import {
     w as ee
-} from "./VBtn-a0da5efe.js";
+} from "./VBtn-49774b84.js";
 import {
     p as U,
     ag as E,
     as as te,
     at as Z,
     ae as k,
     s as D,
@@ -13,15 +13,15 @@
     c as s,
     b as ae,
     r as se,
     aw as $,
     a as R,
     o as ue,
     ax as le
-} from "./index-dcf0de03.js";
+} from "./index-8ef8125d.js";
 const M = Symbol.for("vuetify:layout"),
     X = Symbol.for("vuetify:layout-item"),
     N = 1e3,
     de = U({
         overlaps: {
             type: Array,
             default: () => []
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/logo-c9d5d6ab.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/logo-c9d5d6ab.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/m4a-45331b05.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/m4a-45331b05.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/material-icons-outlined-35dca8a7.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/material-icons-outlined-35dca8a7.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-67d24abe.eot` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-67d24abe.eot`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-80bb28b3.woff` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-80bb28b3.woff`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-a58ecb54.ttf` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-a58ecb54.ttf`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/materialdesignicons-webfont-c1c004a9.woff2` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/materialdesignicons-webfont-c1c004a9.woff2`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/vue-virtual-scroller-4d71315f.css` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/vue-virtual-scroller-4d71315f.css`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/assets/workbox-window.prod.es5-a7b12eab.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/assets/workbox-window.prod.es5-a7b12eab.js`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/favicon.ico` & `music-assistant-frontend-2.0.7/music_assistant_frontend/favicon.ico`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/favicon.svg` & `music-assistant-frontend-2.0.7/music_assistant_frontend/favicon.svg`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/index.html` & `music-assistant-frontend-2.0.7/music_assistant_frontend/index.html`

 * *Files 0% similar despite different names*

```diff
@@ -9,15 +9,15 @@
     <link rel="apple-touch-icon" href="apple-touch-icon.png" sizes="180x180">
     <link rel="mask-icon" href="favicon.svg" color="#FFFFFF">
     <link rel="manifest" href="manifest.webmanifest">
     <meta name="theme-color" content="#ffffff">
     <link rel="icon" href="favicon.ico" />
     <title>Music Assistant</title>
     <meta name="description" content="Music Assistant - Music library manager for Home Assistant">
-    <script type="module" crossorigin src="./assets/index-dcf0de03.js"></script>
+    <script type="module" crossorigin src="./assets/index-8ef8125d.js"></script>
     <link rel="stylesheet" href="./assets/index-4bf8ac1c.css">
   <link rel="manifest" href="./manifest.webmanifest"><style>@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxFIzIFKw-8e48cf20.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxMIzIFKw-638764dc.woff2) format('woff2');unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxEIzIFKw-8007dfe8.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxLIzIFKw-8c3798e3.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxHIzIFKw-ca7eea0c.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+0300-0301,U+0303-0304,U+0308-0309,U+0323,U+0329,U+1EA0-1EF9,U+20AB}@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxGIzIFKw-10b31f4c.woff2) format('woff2');unicode-range:U+0100-02AF,U+0304,U+0308,U+0329,U+1E00-1E9F,U+1EF2-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:Roboto;font-style:normal;font-weight:100;font-display:swap;src:url(./assets/KFOkCnqEu92Fr1MmgVxIIzI-0f303f31.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fCRc4EsA-435e4b7f.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fABc4EsA-47aa3bfa.woff2) format('woff2');unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fCBc4EsA-20dc200c.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fBxc4EsA-455c2c1a.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fCxc4EsA-51f3f418.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+0300-0301,U+0303-0304,U+0308-0309,U+0323,U+0329,U+1EA0-1EF9,U+20AB}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fChc4EsA-b076e863.woff2) format('woff2');unicode-range:U+0100-02AF,U+0304,U+0308,U+0329,U+1E00-1E9F,U+1EF2-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:Roboto;font-style:normal;font-weight:300;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmSU5fBBc4-f7591131.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu72xKOzY-b7ef2cd1.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu5mxKOzY-495d38d4.woff2) format('woff2');unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu7mxKOzY-d368cf5b.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu4WxKOzY-daf51ab5.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu7WxKOzY-77b24796.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+0300-0301,U+0303-0304,U+0308-0309,U+0323,U+0329,U+1EA0-1EF9,U+20AB}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu7GxKOzY-3c23eb02.woff2) format('woff2');unicode-range:U+0100-02AF,U+0304,U+0308,U+0329,U+1E00-1E9F,U+1EF2-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:Roboto;font-style:normal;font-weight:400;font-display:swap;src:url(./assets/KFOmCnqEu92Fr1Mu4mxK-f6734f81.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fCRc4EsA-aeed0e51.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fABc4EsA-3728fbdd.woff2) format('woff2');unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fCBc4EsA-ef8f0236.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fBxc4EsA-713780d8.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fCxc4EsA-0948409a.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+0300-0301,U+0303-0304,U+0308-0309,U+0323,U+0329,U+1EA0-1EF9,U+20AB}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fChc4EsA-7f1c829b.woff2) format('woff2');unicode-range:U+0100-02AF,U+0304,U+0308,U+0329,U+1E00-1E9F,U+1EF2-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:Roboto;font-style:normal;font-weight:500;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmEU9fBBc4-b0195382.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfCRc4EsA-3c505383.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfABc4EsA-6a84eeee.woff2) format('woff2');unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfCBc4EsA-5b6377da.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfBxc4EsA-1c9cc76f.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfCxc4EsA-4ec57f2a.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+0300-0301,U+0303-0304,U+0308-0309,U+0323,U+0329,U+1EA0-1EF9,U+20AB}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfChc4EsA-fc66f942.woff2) format('woff2');unicode-range:U+0100-02AF,U+0304,U+0308,U+0329,U+1E00-1E9F,U+1EF2-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:Roboto;font-style:normal;font-weight:700;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmWUlfBBc4-f5aebdfe.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfCRc4EsA-f265cee6.woff2) format('woff2');unicode-range:U+0460-052F,U+1C80-1C88,U+20B4,U+2DE0-2DFF,U+A640-A69F,U+FE2E-FE2F}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfABc4EsA-9fdb12ce.woff2) format('woff2');unicode-range:U+0301,U+0400-045F,U+0490-0491,U+04B0-04B1,U+2116}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfCBc4EsA-76da333a.woff2) format('woff2');unicode-range:U+1F00-1FFF}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfBxc4EsA-2550c2e2.woff2) format('woff2');unicode-range:U+0370-03FF}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfCxc4EsA-3a38c967.woff2) format('woff2');unicode-range:U+0102-0103,U+0110-0111,U+0128-0129,U+0168-0169,U+01A0-01A1,U+01AF-01B0,U+0300-0301,U+0303-0304,U+0308-0309,U+0323,U+0329,U+1EA0-1EF9,U+20AB}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfChc4EsA-2781e9e7.woff2) format('woff2');unicode-range:U+0100-02AF,U+0304,U+0308,U+0329,U+1E00-1E9F,U+1EF2-1EFF,U+2020,U+20A0-20AB,U+20AD-20CF,U+2113,U+2C60-2C7F,U+A720-A7FF}@font-face{font-family:Roboto;font-style:normal;font-weight:900;font-display:swap;src:url(./assets/KFOlCnqEu92Fr1MmYUtfBBc4-7e262106.woff2) format('woff2');unicode-range:U+0000-00FF,U+0131,U+0152-0153,U+02BB-02BC,U+02C6,U+02DA,U+02DC,U+0304,U+0308,U+0329,U+2000-206F,U+2074,U+20AC,U+2122,U+2191,U+2193,U+2212,U+2215,U+FEFF,U+FFFD}</style></head>
   <body>
     <noscript>
       <strong
         >We're sorry but musicassistant-frontend doesn't work properly without
         JavaScript enabled. Please enable it to continue.</strong
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/manifest.webmanifest` & `music-assistant-frontend-2.0.7/music_assistant_frontend/manifest.webmanifest`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/pwa-192x192.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/pwa-192x192.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/pwa-512x512.png` & `music-assistant-frontend-2.0.7/music_assistant_frontend/pwa-512x512.png`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/sw.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/sw.js`

 * *Files 8% similar despite different names*

#### js-beautify {}

```diff
@@ -26,253 +26,253 @@
     }
 }
 define(["./workbox-27b29e6f"], (function(s) {
     "use strict";
     self.addEventListener("message", (s => {
         s.data && "SKIP_WAITING" === s.data.type && self.skipWaiting()
     })), s.precacheAndRoute([{
-        url: "assets/AddProvider-0b5f3371.js",
+        url: "assets/AddProvider-1cb2a794.js",
         revision: null
     }, {
-        url: "assets/AlbumDetails-8595c1ca.js",
+        url: "assets/AlbumDetails-28f977b9.js",
         revision: null
     }, {
-        url: "assets/Alert-eb81bdeb.js",
+        url: "assets/Alert-bdc4de4a.js",
         revision: null
     }, {
         url: "assets/Alert-eefd31ea.css",
         revision: null
     }, {
-        url: "assets/ArtistDetails-dcd8523b.js",
+        url: "assets/ArtistDetails-b3bb2766.js",
         revision: null
     }, {
-        url: "assets/BrowseView-c902aae4.js",
+        url: "assets/BrowseView-dc407ea0.js",
         revision: null
     }, {
-        url: "assets/Container-8440890a.css",
+        url: "assets/Container-32d4da6e.js",
         revision: null
     }, {
-        url: "assets/Container-d623752d.js",
+        url: "assets/Container-8440890a.css",
         revision: null
     }, {
-        url: "assets/contextmenu-ec34ccac.js",
+        url: "assets/contextmenu-7e32a8e5.js",
         revision: null
     }, {
-        url: "assets/CoreConfigs-6f585b64.js",
+        url: "assets/CoreConfigs-f7edf5eb.js",
         revision: null
     }, {
         url: "assets/CoreConfigs-fc1a0848.css",
         revision: null
     }, {
-        url: "assets/Default-7a0e81ad.js",
+        url: "assets/Default-872711e9.css",
         revision: null
     }, {
-        url: "assets/Default-872711e9.css",
+        url: "assets/Default-e0bfb99e.js",
         revision: null
     }, {
         url: "assets/EditConfig-0f6f6afc.css",
         revision: null
     }, {
-        url: "assets/EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js",
+        url: "assets/EditConfig.vue_vue_type_style_index_0_lang-74792501.js",
         revision: null
     }, {
-        url: "assets/EditCoreConfig-e48660bd.js",
+        url: "assets/EditCoreConfig-b660ec39.js",
         revision: null
     }, {
-        url: "assets/EditPlayer-9b8c67de.js",
+        url: "assets/EditPlayer-7719345f.js",
         revision: null
     }, {
-        url: "assets/EditProvider-f7b6707b.js",
+        url: "assets/EditProvider-7ffddf94.js",
         revision: null
     }, {
         url: "assets/eventbus-d154090d.js",
         revision: null
     }, {
-        url: "assets/HomeView-297a9bbc.js",
+        url: "assets/HomeView-eae672c0.js",
         revision: null
     }, {
         url: "assets/HomeView-f559b858.css",
         revision: null
     }, {
-        url: "assets/index-0afee102.js",
+        url: "assets/index-4bf8ac1c.css",
         revision: null
     }, {
-        url: "assets/index-4bf8ac1c.css",
+        url: "assets/index-8ef8125d.js",
         revision: null
     }, {
-        url: "assets/index-dcf0de03.js",
+        url: "assets/index-a4f9d82d.js",
         revision: null
     }, {
         url: "assets/index.browser-7e542916.js",
         revision: null
     }, {
         url: "assets/ItemsListing-9c236e22.css",
         revision: null
     }, {
-        url: "assets/ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js",
+        url: "assets/ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js",
         revision: null
     }, {
-        url: "assets/layout-087be267.js",
+        url: "assets/layout-2c008654.js",
         revision: null
     }, {
-        url: "assets/LibraryAlbums-e581ef5e.js",
+        url: "assets/LibraryAlbums-cc4c5558.js",
         revision: null
     }, {
-        url: "assets/LibraryArtists-b9bf1b9d.js",
+        url: "assets/LibraryArtists-be2722d0.js",
         revision: null
     }, {
-        url: "assets/LibraryPlaylists-b4797965.js",
+        url: "assets/LibraryPlaylists-14676281.js",
         revision: null
     }, {
-        url: "assets/LibraryRadios-31300560.js",
+        url: "assets/LibraryRadios-d371d843.js",
         revision: null
     }, {
-        url: "assets/LibraryTracks-676be9ae.js",
+        url: "assets/LibraryTracks-ecb94887.js",
         revision: null
     }, {
         url: "assets/ListItem-3da12b03.css",
         revision: null
     }, {
-        url: "assets/ListItem-6dad7331.js",
+        url: "assets/ListItem-bba986fb.js",
         revision: null
     }, {
-        url: "assets/ListviewItem-2c46c8ee.js",
+        url: "assets/ListviewItem-54a3402d.css",
         revision: null
     }, {
-        url: "assets/ListviewItem-54a3402d.css",
+        url: "assets/ListviewItem-ade956db.js",
         revision: null
     }, {
         url: "assets/MediaItemThumb-5ee47663.css",
         revision: null
     }, {
-        url: "assets/MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js",
+        url: "assets/MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js",
         revision: null
     }, {
         url: "assets/PanelviewItem-14a6b77a.css",
         revision: null
     }, {
-        url: "assets/PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js",
+        url: "assets/PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js",
         revision: null
     }, {
-        url: "assets/PlayerQueue-41b4928f.js",
+        url: "assets/PlayerQueue-8c871ec2.js",
         revision: null
     }, {
-        url: "assets/Players-525b85bc.js",
+        url: "assets/Players-2ae3919d.js",
         revision: null
     }, {
-        url: "assets/PlaylistDetails-cce72360.js",
+        url: "assets/PlaylistDetails-971d8698.js",
         revision: null
     }, {
         url: "assets/ProviderDetails-da7f4c54.css",
         revision: null
     }, {
-        url: "assets/ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js",
+        url: "assets/ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js",
         revision: null
     }, {
-        url: "assets/Providers-3598c1f3.js",
+        url: "assets/Providers-3820a270.css",
         revision: null
     }, {
-        url: "assets/Providers-3820a270.css",
+        url: "assets/Providers-453e3025.js",
         revision: null
     }, {
-        url: "assets/RadioDetails-993d50b0.js",
+        url: "assets/RadioDetails-6761105c.js",
         revision: null
     }, {
-        url: "assets/Search-433484bb.js",
+        url: "assets/Search-93fe9303.js",
         revision: null
     }, {
-        url: "assets/Settings-70d67eb6.js",
+        url: "assets/Settings-ef547e38.js",
         revision: null
     }, {
-        url: "assets/TrackDetails-95dc4644.js",
+        url: "assets/TrackDetails-807370a0.js",
         revision: null
     }, {
         url: "assets/VBadge-4ff04865.css",
         revision: null
     }, {
-        url: "assets/VBadge-8be61727.js",
+        url: "assets/VBadge-8b6f3afa.js",
         revision: null
     }, {
-        url: "assets/VBtn-a0da5efe.js",
+        url: "assets/VBtn-49774b84.js",
         revision: null
     }, {
         url: "assets/VBtn-fccecd75.css",
         revision: null
     }, {
-        url: "assets/VCard-111cabcf.js",
+        url: "assets/VCard-790bb5b3.css",
         revision: null
     }, {
-        url: "assets/VCard-790bb5b3.css",
+        url: "assets/VCard-e81591ba.js",
         revision: null
     }, {
-        url: "assets/VCheckboxBtn-d54a899d.js",
+        url: "assets/VCheckboxBtn-4c08e900.js",
         revision: null
     }, {
         url: "assets/VCheckboxBtn-e9f604b5.css",
         revision: null
     }, {
-        url: "assets/VDialog-ccbfddc9.js",
+        url: "assets/VDialog-b35e6970.js",
         revision: null
     }, {
         url: "assets/VDialog-ff1232cf.css",
         revision: null
     }, {
-        url: "assets/VExpansionPanel-286d9c63.js",
+        url: "assets/VExpansionPanel-2b4b0a5a.css",
         revision: null
     }, {
-        url: "assets/VExpansionPanel-2b4b0a5a.css",
+        url: "assets/VExpansionPanel-523a6df6.js",
         revision: null
     }, {
         url: "assets/VGrid-ec674b79.css",
         revision: null
     }, {
         url: "assets/VListItem-028a8916.css",
         revision: null
     }, {
-        url: "assets/VListItem-943ee224.js",
+        url: "assets/VListItem-b049d12d.js",
         revision: null
     }, {
-        url: "assets/VMenu-3bdd1b96.js",
+        url: "assets/VMenu-87d759b1.css",
         revision: null
     }, {
-        url: "assets/VMenu-87d759b1.css",
+        url: "assets/VMenu-a805d6b6.js",
         revision: null
     }, {
-        url: "assets/VRow-73379099.js",
+        url: "assets/VRow-08fca7f1.js",
         revision: null
     }, {
-        url: "assets/VSpacer-4e341220.js",
+        url: "assets/VSpacer-b8926de0.js",
         revision: null
     }, {
-        url: "assets/VTabs-7c03bdc8.js",
+        url: "assets/VTabs-1b99b0fa.js",
         revision: null
     }, {
         url: "assets/VTabs-f9f04fad.css",
         revision: null
     }, {
         url: "assets/VTextField-6adde8bb.css",
         revision: null
     }, {
-        url: "assets/VTextField-f81f9175.js",
+        url: "assets/VTextField-be284f64.js",
         revision: null
     }, {
         url: "assets/VToolbar-aa2d1d9a.css",
         revision: null
     }, {
-        url: "assets/VToolbar-dfba6de4.js",
+        url: "assets/VToolbar-b4c95f12.js",
         revision: null
     }, {
         url: "assets/vue-virtual-scroller-4d71315f.css",
         revision: null
     }, {
         url: "assets/workbox-window.prod.es5-a7b12eab.js",
         revision: null
     }, {
         url: "index.html",
-        revision: "732b2bb2aec3f155a50c1f9e8e754f88"
+        revision: "f379110342ee4bc782f64770db7036ea"
     }, {
         url: "favicon.svg",
         revision: "ecfda4076e793b6ffd619ed24e66c36d"
     }, {
         url: "favicon.ico",
         revision: "60d77c1713c2255be3f6de69c4de24d9"
     }, {
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend/workbox-27b29e6f.js` & `music-assistant-frontend-2.0.7/music_assistant_frontend/workbox-27b29e6f.js`

 * *Files identical despite different names*

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/PKG-INFO` & `music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: music-assistant-frontend
-Version: 2.0.6
+Version: 2.0.7
 Summary: The Music Assistant frontend
 Author-email: The Music Assistant Authors <m.vanderveldt@outlook.com>
 License: Apache-2.0
 Project-URL: Homepage, https://github.com/music-assistant/frontend
 Platform: any
 Requires-Python: >=3.9.0
 Description-Content-Type: text/markdown
```

### Comparing `music-assistant-frontend-2.0.6/music_assistant_frontend.egg-info/SOURCES.txt` & `music-assistant-frontend-2.0.7/music_assistant_frontend.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -16,35 +16,35 @@
 music_assistant_frontend/sw.js
 music_assistant_frontend/workbox-27b29e6f.js
 music_assistant_frontend.egg-info/PKG-INFO
 music_assistant_frontend.egg-info/SOURCES.txt
 music_assistant_frontend.egg-info/dependency_links.txt
 music_assistant_frontend.egg-info/not-zip-safe
 music_assistant_frontend.egg-info/top_level.txt
-music_assistant_frontend/assets/AddProvider-0b5f3371.js
-music_assistant_frontend/assets/AlbumDetails-8595c1ca.js
-music_assistant_frontend/assets/Alert-eb81bdeb.js
+music_assistant_frontend/assets/AddProvider-1cb2a794.js
+music_assistant_frontend/assets/AlbumDetails-28f977b9.js
+music_assistant_frontend/assets/Alert-bdc4de4a.js
 music_assistant_frontend/assets/Alert-eefd31ea.css
-music_assistant_frontend/assets/ArtistDetails-dcd8523b.js
-music_assistant_frontend/assets/BrowseView-c902aae4.js
+music_assistant_frontend/assets/ArtistDetails-b3bb2766.js
+music_assistant_frontend/assets/BrowseView-dc407ea0.js
+music_assistant_frontend/assets/Container-32d4da6e.js
 music_assistant_frontend/assets/Container-8440890a.css
-music_assistant_frontend/assets/Container-d623752d.js
-music_assistant_frontend/assets/CoreConfigs-6f585b64.js
+music_assistant_frontend/assets/CoreConfigs-f7edf5eb.js
 music_assistant_frontend/assets/CoreConfigs-fc1a0848.css
-music_assistant_frontend/assets/Default-7a0e81ad.js
 music_assistant_frontend/assets/Default-872711e9.css
+music_assistant_frontend/assets/Default-e0bfb99e.js
 music_assistant_frontend/assets/EditConfig-0f6f6afc.css
-music_assistant_frontend/assets/EditConfig.vue_vue_type_style_index_0_lang-80768ce3.js
-music_assistant_frontend/assets/EditCoreConfig-e48660bd.js
-music_assistant_frontend/assets/EditPlayer-9b8c67de.js
-music_assistant_frontend/assets/EditProvider-f7b6707b.js
-music_assistant_frontend/assets/HomeView-297a9bbc.js
+music_assistant_frontend/assets/EditConfig.vue_vue_type_style_index_0_lang-74792501.js
+music_assistant_frontend/assets/EditCoreConfig-b660ec39.js
+music_assistant_frontend/assets/EditPlayer-7719345f.js
+music_assistant_frontend/assets/EditProvider-7ffddf94.js
+music_assistant_frontend/assets/HomeView-eae672c0.js
 music_assistant_frontend/assets/HomeView-f559b858.css
 music_assistant_frontend/assets/ItemsListing-9c236e22.css
-music_assistant_frontend/assets/ItemsListing.vue_vue_type_style_index_0_lang-38bc2f50.js
+music_assistant_frontend/assets/ItemsListing.vue_vue_type_style_index_0_lang-8e142c2f.js
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxEIzIFKw-8007dfe8.woff2
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxFIzIFKw-8e48cf20.woff2
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxGIzIFKw-10b31f4c.woff2
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxHIzIFKw-ca7eea0c.woff2
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxIIzI-0f303f31.woff2
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxLIzIFKw-8c3798e3.woff2
 music_assistant_frontend/assets/KFOkCnqEu92Fr1MmgVxMIzIFKw-638764dc.woff2
@@ -79,79 +79,79 @@
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4WxKOzY-daf51ab5.woff2
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu4mxK-f6734f81.woff2
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu5mxKOzY-495d38d4.woff2
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu72xKOzY-b7ef2cd1.woff2
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7GxKOzY-3c23eb02.woff2
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7WxKOzY-77b24796.woff2
 music_assistant_frontend/assets/KFOmCnqEu92Fr1Mu7mxKOzY-d368cf5b.woff2
-music_assistant_frontend/assets/LibraryAlbums-e581ef5e.js
-music_assistant_frontend/assets/LibraryArtists-b9bf1b9d.js
-music_assistant_frontend/assets/LibraryPlaylists-b4797965.js
-music_assistant_frontend/assets/LibraryRadios-31300560.js
-music_assistant_frontend/assets/LibraryTracks-676be9ae.js
+music_assistant_frontend/assets/LibraryAlbums-cc4c5558.js
+music_assistant_frontend/assets/LibraryArtists-be2722d0.js
+music_assistant_frontend/assets/LibraryPlaylists-14676281.js
+music_assistant_frontend/assets/LibraryRadios-d371d843.js
+music_assistant_frontend/assets/LibraryTracks-ecb94887.js
 music_assistant_frontend/assets/ListItem-3da12b03.css
-music_assistant_frontend/assets/ListItem-6dad7331.js
-music_assistant_frontend/assets/ListviewItem-2c46c8ee.js
+music_assistant_frontend/assets/ListItem-bba986fb.js
 music_assistant_frontend/assets/ListviewItem-54a3402d.css
+music_assistant_frontend/assets/ListviewItem-ade956db.js
 music_assistant_frontend/assets/MaterialIcons-Regular-11ec382a.woff
 music_assistant_frontend/assets/MaterialIcons-Regular-29c11fa5.ttf
 music_assistant_frontend/assets/MaterialIcons-Regular-5743ed3d.woff2
 music_assistant_frontend/assets/MaterialIcons-Regular-e69d687a.eot
 music_assistant_frontend/assets/MediaItemThumb-5ee47663.css
-music_assistant_frontend/assets/MediaItemThumb.vue_vue_type_style_index_0_lang-b38d9ae1.js
+music_assistant_frontend/assets/MediaItemThumb.vue_vue_type_style_index_0_lang-3622812c.js
 music_assistant_frontend/assets/PanelviewItem-14a6b77a.css
-music_assistant_frontend/assets/PanelviewItem.vue_vue_type_style_index_0_lang-44df1bef.js
-music_assistant_frontend/assets/PlayerQueue-41b4928f.js
-music_assistant_frontend/assets/Players-525b85bc.js
-music_assistant_frontend/assets/PlaylistDetails-cce72360.js
+music_assistant_frontend/assets/PanelviewItem.vue_vue_type_style_index_0_lang-a068cbe2.js
+music_assistant_frontend/assets/PlayerQueue-8c871ec2.js
+music_assistant_frontend/assets/Players-2ae3919d.js
+music_assistant_frontend/assets/PlaylistDetails-971d8698.js
 music_assistant_frontend/assets/ProviderDetails-da7f4c54.css
-music_assistant_frontend/assets/ProviderDetails.vue_vue_type_script_setup_true_lang-1829229a.js
-music_assistant_frontend/assets/Providers-3598c1f3.js
+music_assistant_frontend/assets/ProviderDetails.vue_vue_type_script_setup_true_lang-86038b27.js
 music_assistant_frontend/assets/Providers-3820a270.css
-music_assistant_frontend/assets/RadioDetails-993d50b0.js
-music_assistant_frontend/assets/Search-433484bb.js
-music_assistant_frontend/assets/Settings-70d67eb6.js
-music_assistant_frontend/assets/TrackDetails-95dc4644.js
+music_assistant_frontend/assets/Providers-453e3025.js
+music_assistant_frontend/assets/RadioDetails-6761105c.js
+music_assistant_frontend/assets/Search-93fe9303.js
+music_assistant_frontend/assets/Settings-ef547e38.js
+music_assistant_frontend/assets/TrackDetails-807370a0.js
 music_assistant_frontend/assets/VBadge-4ff04865.css
-music_assistant_frontend/assets/VBadge-8be61727.js
-music_assistant_frontend/assets/VBtn-a0da5efe.js
+music_assistant_frontend/assets/VBadge-8b6f3afa.js
+music_assistant_frontend/assets/VBtn-49774b84.js
 music_assistant_frontend/assets/VBtn-fccecd75.css
-music_assistant_frontend/assets/VCard-111cabcf.js
 music_assistant_frontend/assets/VCard-790bb5b3.css
-music_assistant_frontend/assets/VCheckboxBtn-d54a899d.js
+music_assistant_frontend/assets/VCard-e81591ba.js
+music_assistant_frontend/assets/VCheckboxBtn-4c08e900.js
 music_assistant_frontend/assets/VCheckboxBtn-e9f604b5.css
-music_assistant_frontend/assets/VDialog-ccbfddc9.js
+music_assistant_frontend/assets/VDialog-b35e6970.js
 music_assistant_frontend/assets/VDialog-ff1232cf.css
-music_assistant_frontend/assets/VExpansionPanel-286d9c63.js
 music_assistant_frontend/assets/VExpansionPanel-2b4b0a5a.css
+music_assistant_frontend/assets/VExpansionPanel-523a6df6.js
 music_assistant_frontend/assets/VGrid-ec674b79.css
 music_assistant_frontend/assets/VListItem-028a8916.css
-music_assistant_frontend/assets/VListItem-943ee224.js
-music_assistant_frontend/assets/VMenu-3bdd1b96.js
+music_assistant_frontend/assets/VListItem-b049d12d.js
 music_assistant_frontend/assets/VMenu-87d759b1.css
-music_assistant_frontend/assets/VRow-73379099.js
-music_assistant_frontend/assets/VSpacer-4e341220.js
-music_assistant_frontend/assets/VTabs-7c03bdc8.js
+music_assistant_frontend/assets/VMenu-a805d6b6.js
+music_assistant_frontend/assets/VRow-08fca7f1.js
+music_assistant_frontend/assets/VSpacer-b8926de0.js
+music_assistant_frontend/assets/VTabs-1b99b0fa.js
 music_assistant_frontend/assets/VTabs-f9f04fad.css
 music_assistant_frontend/assets/VTextField-6adde8bb.css
-music_assistant_frontend/assets/VTextField-f81f9175.js
+music_assistant_frontend/assets/VTextField-be284f64.js
 music_assistant_frontend/assets/VToolbar-aa2d1d9a.css
-music_assistant_frontend/assets/VToolbar-dfba6de4.js
-music_assistant_frontend/assets/contextmenu-ec34ccac.js
+music_assistant_frontend/assets/VToolbar-b4c95f12.js
+music_assistant_frontend/assets/contextmenu-7e32a8e5.js
 music_assistant_frontend/assets/cover_dark-75402cd0.png
 music_assistant_frontend/assets/cover_light-b832ae9e.png
 music_assistant_frontend/assets/crossfade-ba51f69a.png
 music_assistant_frontend/assets/eventbus-d154090d.js
 music_assistant_frontend/assets/hires-438c7046.png
-music_assistant_frontend/assets/index-0afee102.js
 music_assistant_frontend/assets/index-4bf8ac1c.css
-music_assistant_frontend/assets/index-dcf0de03.js
+music_assistant_frontend/assets/index-8ef8125d.js
+music_assistant_frontend/assets/index-a4f9d82d.js
 music_assistant_frontend/assets/index.browser-7e542916.js
 music_assistant_frontend/assets/info_gradient-a4aefd1d.jpg
-music_assistant_frontend/assets/layout-087be267.js
+music_assistant_frontend/assets/layout-2c008654.js
 music_assistant_frontend/assets/logo-c9d5d6ab.png
 music_assistant_frontend/assets/m4a-45331b05.png
 music_assistant_frontend/assets/material-icons-outlined-35dca8a7.woff2
 music_assistant_frontend/assets/materialdesignicons-webfont-67d24abe.eot
 music_assistant_frontend/assets/materialdesignicons-webfont-80bb28b3.woff
 music_assistant_frontend/assets/materialdesignicons-webfont-a58ecb54.ttf
 music_assistant_frontend/assets/materialdesignicons-webfont-c1c004a9.woff2
```

### Comparing `music-assistant-frontend-2.0.6/pyproject.toml` & `music-assistant-frontend-2.0.7/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -3,15 +3,15 @@
     "setuptools~=62.3",
     "wheel~=0.37.1",
 ]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "music-assistant-frontend"
-version = "2.0.6"
+version = "2.0.7"
 description = "The Music Assistant frontend"
 readme = "README.md"
 authors = [
     { name = "The Music Assistant Authors", email = "m.vanderveldt@outlook.com" },
 ]
 requires-python = ">=3.9.0"
```

