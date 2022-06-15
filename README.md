# regex-awesome

English | [中文](./README_zh-CN.md)

## ⚠️ Pull Reqeust Wantted !!!

I created this repo to share regex rules we may use, I'm going to improve and fix these rules, and add more rules , if you find any
problem(a wrong rule; a simplable rule) or just wand to make it better, create a pull request and I would merge if it's ok
, thanks!

## Numbers

### All positive integers and floats

**Pattern** `/^(0|[1-9]\d*)(\.\d*[1-9])?$/`

**Tests**

- ❌ `0123` (leading `0` not allowed)
- ❌ `123.` (point without fraction part not allowed)
- ❌ `123.0` (one or more `0` as fraction part not allowed)
- ✅ `123.01`

## Url & Path

### ❓Email addresses

Check full description for email addresses, [Click](https://en.wikipedia.org/wiki/Email_address), But it's too complex. So here We
use the gmail rules, ie "only letters, numbers and periods(.) allowed, periods(.) not allowed at first and last place, and can't be consecutive."

> Here we won't check the `@` character and domain part.

**Pattern** `/^[A-Za-z0-9]+(\.[A-Za-z0-9])*$/`

**Tests**

- ❌ `abc` `.abc` `a..bc` `abc.`
- ✅ `abc` `a.bc` `a.b.c`
