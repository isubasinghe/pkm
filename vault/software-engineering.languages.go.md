---
id: Id7BxIuzwUcQaw6KDKdzp
title: Go
desc: ''
updated: 1642230824126
created: 1642230589198
---

## Representing Sum Types 
My personal opinion is that it does not make sense 
to use interfaces{} to represent sum types. It makes things such as Unmarshalling annoying and cubersome to use since 
it requires an intermediate type to unmarshal to first. Using a product type (struct) with a flag to indicate the actual type in use 
is more convenient. 
