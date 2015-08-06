# Git diff

Three dots
```
git diff master...develop
```
shows what changed on develop since you forked from master (basically it diffs against how master looked _when you branched_) whereas two dots

```
git diff master..develop
```
or just
```
git diff master develop
```
 shows the difference from master _right now_.
