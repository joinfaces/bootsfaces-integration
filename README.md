# BootsFaces integration

As well as ButterFaces [BootsFaces](http://www.bootsfaces.net/) comes with jQuery and Bootstrap. This does not work out of the box.

## Problem
ButterFaces deliveres css and javascript as first part of html head to allow custom class handling. BootsFaces deliveres its own jQuery after ButterFaces, so ButterFaces jQuery plugins does not work anymore.

## Solution
Disable jQuery in BootsFaces and most thinks will work
```yml
jsf:
  bootsfaces:
    get_jquery_from_cdn: yes
    getBootstrapFromCdn: yes
```

## Start showcase
```
java -jar target/BootsFacesIntegration-1.0-SNAPSHOT.jar
```

## Known problems
BootsFaces and ButterFaces override some Bootstrap style sheet. Sometimes they come in the transverse, i.e. placeholder position in ButterFaces. We are working on that.
