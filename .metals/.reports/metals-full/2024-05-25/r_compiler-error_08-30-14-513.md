file://<WORKSPACE>/build.sbt
### java.lang.AssertionError: assertion failed: denotation module class ProcessBuilder$ invalid in run 6. ValidFor: Period(1..2, run = 14)

occurred in the presentation compiler.

presentation compiler configuration:
Scala version: 3.3.3
Classpath:
<HOME>/Library/Caches/Coursier/v1/https/repo1.maven.org/maven2/org/scala-lang/scala3-library_3/3.3.3/scala3-library_3-3.3.3.jar [exists ], <HOME>/Library/Caches/Coursier/v1/https/repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.12/scala-library-2.13.12.jar [exists ]
Options:



action parameters:
offset: 5
uri: file://<WORKSPACE>/build.sbt
text:
```scala
ThisB@@

```



#### Error stacktrace:

```
scala.runtime.Scala3RunTime$.assertFailed(Scala3RunTime.scala:8)
	dotty.tools.dotc.core.Denotations$SingleDenotation.updateValidity(Denotations.scala:717)
	dotty.tools.dotc.core.Denotations$SingleDenotation.bringForward(Denotations.scala:742)
	dotty.tools.dotc.core.Denotations$SingleDenotation.toNewRun$1(Denotations.scala:799)
	dotty.tools.dotc.core.Denotations$SingleDenotation.current(Denotations.scala:870)
	dotty.tools.dotc.core.Symbols$Symbol.recomputeDenot(Symbols.scala:120)
	dotty.tools.dotc.core.Symbols$Symbol.computeDenot(Symbols.scala:114)
	dotty.tools.dotc.core.Symbols$Symbol.denot(Symbols.scala:107)
	dotty.tools.dotc.core.Symbols$Symbol.name(Symbols.scala:260)
	scala.meta.internal.pc.IndexedContext$.fromImportInfo$1$$anonfun$1(IndexedContext.scala:192)
	scala.collection.immutable.List.filter(List.scala:529)
	scala.meta.internal.pc.IndexedContext$.allAccessibleSymbols$1(IndexedContext.scala:168)
	scala.meta.internal.pc.IndexedContext$.fromImportInfo$1(IndexedContext.scala:193)
	scala.meta.internal.pc.IndexedContext$.scala$meta$internal$pc$IndexedContext$$$extractNames(IndexedContext.scala:210)
	scala.meta.internal.pc.IndexedContext$LazyWrapper.<init>(IndexedContext.scala:100)
	scala.meta.internal.pc.IndexedContext$.apply(IndexedContext.scala:88)
	scala.meta.internal.pc.IndexedContext$LazyWrapper.<init>(IndexedContext.scala:99)
	scala.meta.internal.pc.IndexedContext$.apply(IndexedContext.scala:88)
	scala.meta.internal.pc.IndexedContext$LazyWrapper.<init>(IndexedContext.scala:99)
	scala.meta.internal.pc.IndexedContext$.apply(IndexedContext.scala:88)
	scala.meta.internal.pc.IndexedContext$LazyWrapper.<init>(IndexedContext.scala:99)
	scala.meta.internal.pc.IndexedContext$.apply(IndexedContext.scala:88)
	scala.meta.internal.pc.IndexedContext$LazyWrapper.<init>(IndexedContext.scala:99)
	scala.meta.internal.pc.IndexedContext$.apply(IndexedContext.scala:88)
	scala.meta.internal.pc.IndexedContext$LazyWrapper.<init>(IndexedContext.scala:99)
	scala.meta.internal.pc.IndexedContext$.apply(IndexedContext.scala:88)
	scala.meta.internal.pc.completions.CompletionProvider.completions(CompletionProvider.scala:62)
	scala.meta.internal.pc.ScalaPresentationCompiler.complete$$anonfun$1(ScalaPresentationCompiler.scala:147)
```
#### Short summary: 

java.lang.AssertionError: assertion failed: denotation module class ProcessBuilder$ invalid in run 6. ValidFor: Period(1..2, run = 14)