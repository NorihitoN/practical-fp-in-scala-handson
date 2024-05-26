file://<WORKSPACE>/build.sbt
### java.lang.AssertionError: assertion failed: denotation module class Tuple3Zipped$ invalid in run 1. ValidFor: Period(1..5, run = 3)

occurred in the presentation compiler.

presentation compiler configuration:
Scala version: 3.3.3
Classpath:
<HOME>/Library/Caches/Coursier/v1/https/repo1.maven.org/maven2/org/scala-lang/scala3-library_3/3.3.3/scala3-library_3-3.3.3.jar [exists ], <HOME>/Library/Caches/Coursier/v1/https/repo1.maven.org/maven2/org/scala-lang/scala-library/2.13.12/scala-library-2.13.12.jar [exists ]
Options:



action parameters:
offset: 210
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
      compoi@@
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
	dotty.tools.dotc.core.Symbols$.toDenot(Symbols.scala:494)
	dotty.tools.dotc.core.Definitions.isVarArityClass(Definitions.scala:1520)
	dotty.tools.dotc.core.Definitions.isTupleClass(Definitions.scala:1576)
	dotty.tools.dotc.core.Definitions.adjustForTuple(Definitions.scala:1895)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$.setClassInfo(Scala2Unpickler.scala:106)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.parseToCompletion$1(Scala2Unpickler.scala:615)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.complete$$anonfun$1(Scala2Unpickler.scala:645)
	scala.runtime.java8.JFunction0$mcV$sp.apply(JFunction0$mcV$sp.scala:18)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.atReadPos(Scala2Unpickler.scala:318)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.complete(Scala2Unpickler.scala:647)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.completeFrom(SymDenotations.scala:174)
	dotty.tools.dotc.core.Denotations$Denotation.completeInfo$1(Denotations.scala:187)
	dotty.tools.dotc.core.Denotations$Denotation.info(Denotations.scala:189)
	dotty.tools.dotc.core.Denotations$Denotation.completeInfo$1(Denotations.scala:187)
	dotty.tools.dotc.core.Denotations$Denotation.info(Denotations.scala:189)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.declIn$1(Scala2Unpickler.scala:376)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.fromName$1(Scala2Unpickler.scala:377)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readExtSymbol$1(Scala2Unpickler.scala:408)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readDisambiguatedSymbol(Scala2Unpickler.scala:435)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readSymbol(Scala2Unpickler.scala:336)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readSymbolRef(Scala2Unpickler.scala:947)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readType(Scala2Unpickler.scala:801)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readTypeRef$$anonfun$1(Scala2Unpickler.scala:959)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.atReadPos(Scala2Unpickler.scala:318)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.at(Scala2Unpickler.scala:308)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readTypeRef(Scala2Unpickler.scala:959)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readType(Scala2Unpickler.scala:856)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readTypeRef$$anonfun$1(Scala2Unpickler.scala:959)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.atReadPos(Scala2Unpickler.scala:318)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.at(Scala2Unpickler.scala:308)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readTypeRef(Scala2Unpickler.scala:959)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.readType(Scala2Unpickler.scala:870)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.$anonfun$6(Scala2Unpickler.scala:605)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.atReadPos(Scala2Unpickler.scala:318)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.at(Scala2Unpickler.scala:308)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.parseToCompletion$1(Scala2Unpickler.scala:605)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.complete$$anonfun$1(Scala2Unpickler.scala:645)
	scala.runtime.java8.JFunction0$mcV$sp.apply(JFunction0$mcV$sp.scala:18)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler.atReadPos(Scala2Unpickler.scala:318)
	dotty.tools.dotc.core.unpickleScala2.Scala2Unpickler$LocalUnpickler.complete(Scala2Unpickler.scala:647)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.completeFrom(SymDenotations.scala:174)
	dotty.tools.dotc.core.Denotations$Denotation.completeInfo$1(Denotations.scala:187)
	dotty.tools.dotc.core.Denotations$Denotation.info(Denotations.scala:189)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.ensureCompleted(SymDenotations.scala:393)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.flags(SymDenotations.scala:66)
	dotty.tools.dotc.core.SymDenotations$SymDenotation.is(SymDenotations.scala:112)
	dotty.tools.dotc.interactive.Completion$Completer.dotty$tools$dotc$interactive$Completion$Completer$$include(Completion.scala:465)
	dotty.tools.dotc.interactive.Completion$Completer.$anonfun$5(Completion.scala:350)
	scala.collection.immutable.List.filter(List.scala:515)
	dotty.tools.dotc.interactive.Completion$Completer.importedCompletions(Completion.scala:350)
	dotty.tools.dotc.interactive.Completion$Completer.scopeCompletions$$anonfun$1(Completion.scala:240)
	scala.runtime.function.JProcedure1.apply(JProcedure1.java:15)
	scala.runtime.function.JProcedure1.apply(JProcedure1.java:10)
	scala.collection.IterableOnceOps.foreach(IterableOnce.scala:576)
	scala.collection.IterableOnceOps.foreach$(IterableOnce.scala:574)
	dotty.tools.dotc.core.Contexts$Context$$anon$2.foreach(Contexts.scala:132)
	dotty.tools.dotc.interactive.Completion$Completer.scopeCompletions(Completion.scala:254)
	dotty.tools.dotc.interactive.Completion$.computeCompletions(Completion.scala:149)
	dotty.tools.dotc.interactive.Completion$.completions(Completion.scala:50)
	scala.meta.internal.pc.completions.Completions.completions(Completions.scala:202)
	scala.meta.internal.pc.completions.CompletionProvider.completions(CompletionProvider.scala:86)
	scala.meta.internal.pc.ScalaPresentationCompiler.complete$$anonfun$1(ScalaPresentationCompiler.scala:147)
```
#### Short summary: 

java.lang.AssertionError: assertion failed: denotation module class Tuple3Zipped$ invalid in run 1. ValidFor: Period(1..5, run = 3)