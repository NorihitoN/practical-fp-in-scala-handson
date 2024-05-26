file://<WORKSPACE>/build.sbt
### java.lang.AssertionError: assertion failed: denotation class deprecated invalid in run 7. ValidFor: Period(1..2, run = 8)

occurred in the presentation compiler.

presentation compiler configuration:
Scala version: 3.3.3
Classpath:
<HOME>/Library/Caches/Coursier/v1/https/repo1.maven.org/maven2/org/scala-lang/scala3-library_3/3.3.3/scala3-library_3-3.3.3.jar [exists ], <HOME>/Library/Caches/Coursier/v1/https/repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.12/scala-library-2.13.12.jar [exists ]
Options:



action parameters:
offset: 205
uri: file://<WORKSPACE>/build.sbt
text:
```scala
ThisBuild / scalaVersion := "2.13.5"

lazy val root = (project in file("."))
  .settings(
    name := "minimal",
    version := "0.1",
    scalaVersion := "2.13.5",
    libraryDependencies ++= Seq(
      c@@
    )
  )

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
	dotty.tools.dotc.core.Annotations$LazyAnnotation.symbol(Annotations.scala:129)
	dotty.tools.dotc.core.Annotations$Annotation.matches(Annotations.scala:26)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.dropOtherAnnotations(SymDenotations.scala:307)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.unforcedAnnotation(SymDenotations.scala:278)
	dotty.tools.dotc.core.Symbols$ClassSymbol.sourceOfClass(Symbols.scala:471)
	dotty.tools.dotc.core.Symbols$Symbol.source(Symbols.scala:297)
	dotty.tools.dotc.core.Symbols$Symbol.source(Symbols.scala:294)
	dotty.tools.dotc.core.Symbols$Symbol.source(Symbols.scala:294)
	scala.meta.internal.pc.completions.Completions.symbolRelevance$1(Completions.scala:760)
	scala.meta.internal.pc.completions.Completions.scala$meta$internal$pc$completions$Completions$$computeRelevancePenalty(Completions.scala:806)
	scala.meta.internal.pc.completions.Completions$$anon$4.compareByRelevance(Completions.scala:890)
	scala.meta.internal.pc.completions.Completions$$anon$4.compare(Completions.scala:978)
	scala.meta.internal.pc.completions.Completions$$anon$4.compare(Completions.scala:959)
	java.base/java.util.TimSort.countRunAndMakeAscending(TimSort.java:360)
	java.base/java.util.TimSort.sort(TimSort.java:220)
	java.base/java.util.Arrays.sort(Arrays.java:1233)
	scala.collection.SeqOps.sorted(Seq.scala:728)
	scala.collection.SeqOps.sorted$(Seq.scala:719)
	scala.collection.immutable.List.scala$collection$immutable$StrictOptimizedSeqOps$$super$sorted(List.scala:79)
	scala.collection.immutable.StrictOptimizedSeqOps.sorted(StrictOptimizedSeqOps.scala:78)
	scala.collection.immutable.StrictOptimizedSeqOps.sorted$(StrictOptimizedSeqOps.scala:78)
	scala.collection.immutable.List.sorted(List.scala:79)
	scala.meta.internal.pc.completions.Completions.completions(Completions.scala:210)
	scala.meta.internal.pc.completions.CompletionProvider.completions(CompletionProvider.scala:86)
	scala.meta.internal.pc.ScalaPresentationCompiler.complete$$anonfun$1(ScalaPresentationCompiler.scala:147)
```
#### Short summary: 

java.lang.AssertionError: assertion failed: denotation class deprecated invalid in run 7. ValidFor: Period(1..2, run = 8)