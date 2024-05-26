file://<WORKSPACE>/build.sbt
### java.lang.AssertionError: assertion failed: denotation class RichInt invalid in run 1. ValidFor: Period(1..5, run = 3)

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
      compil@@
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
	dotty.tools.dotc.core.Types$NamedType.info(Types.scala:2340)
	dotty.tools.dotc.core.Types$TermLambda.dotty$tools$dotc$core$Types$TermLambda$$_$compute$1(Types.scala:3859)
	dotty.tools.dotc.core.Types$TermLambda.dotty$tools$dotc$core$Types$TermLambda$$depStatus(Types.scala:3886)
	dotty.tools.dotc.core.Types$TermLambda.dependencyStatus(Types.scala:3900)
	dotty.tools.dotc.core.Types$TermLambda.resultType(Types.scala:3824)
	dotty.tools.dotc.core.Types$TermLambda.resultType$(Types.scala:3816)
	dotty.tools.dotc.core.Types$MethodType.resultType(Types.scala:3961)
	dotty.tools.dotc.core.Types$TypeMap.mapOverLambda(Types.scala:5738)
	dotty.tools.dotc.core.TypeOps$AsSeenFromMap.apply(TypeOps.scala:105)
	dotty.tools.dotc.core.TypeOps$.asSeenFrom(TypeOps.scala:56)
	dotty.tools.dotc.core.Types$Type.asSeenFrom(Types.scala:1054)
	dotty.tools.dotc.core.Denotations$SingleDenotation.derived$1(Denotations.scala:1090)
	dotty.tools.dotc.core.Denotations$SingleDenotation.computeAsSeenFrom(Denotations.scala:1117)
	dotty.tools.dotc.core.Denotations$SingleDenotation.computeAsSeenFrom(Denotations.scala:1070)
	dotty.tools.dotc.core.Denotations$PreDenotation.asSeenFrom(Denotations.scala:134)
	dotty.tools.dotc.core.Denotations$SingleDenotation.mapInherited(Denotations.scala:1052)
	dotty.tools.dotc.core.Denotations$SingleDenotation.mapInherited(Denotations.scala:1049)
	dotty.tools.dotc.core.SymDenotations$ClassDenotation.collect$1(SymDenotations.scala:2158)
	dotty.tools.dotc.core.SymDenotations$ClassDenotation.addInherited(SymDenotations.scala:2163)
	dotty.tools.dotc.core.SymDenotations$ClassDenotation.computeMembersNamed(SymDenotations.scala:2148)
	dotty.tools.dotc.core.SymDenotations$ClassDenotation.membersNamed(SymDenotations.scala:2115)
	dotty.tools.dotc.core.SymDenotations$ClassDenotation.findMember(SymDenotations.scala:2166)
	dotty.tools.dotc.core.Types$Type.go$1(Types.scala:721)
	dotty.tools.dotc.core.Types$Type.findMember(Types.scala:900)
	dotty.tools.dotc.core.Types$Type.memberBasedOnFlags(Types.scala:704)
	dotty.tools.dotc.core.Types$Type.member(Types.scala:688)
	dotty.tools.dotc.core.Types$Type.implicitMembers$$anonfun$1(Types.scala:1014)
	scala.runtime.function.JProcedure2.apply(JProcedure2.java:15)
	scala.runtime.function.JProcedure2.apply(JProcedure2.java:10)
	dotty.tools.dotc.core.Types$Type.memberDenots$$anonfun$1(Types.scala:946)
	scala.runtime.function.JProcedure1.apply(JProcedure1.java:15)
	scala.runtime.function.JProcedure1.apply(JProcedure1.java:10)
	scala.collection.immutable.HashSet.foreach(HashSet.scala:958)
	dotty.tools.dotc.core.Types$Type.memberDenots(Types.scala:946)
	dotty.tools.dotc.core.Types$Type.implicitMembers(Types.scala:1014)
	dotty.tools.dotc.typer.ImportInfo.importedImplicits(ImportInfo.scala:132)
	dotty.tools.dotc.interactive.Completion$Completer.importedCompletions(Completion.scala:348)
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

java.lang.AssertionError: assertion failed: denotation class RichInt invalid in run 1. ValidFor: Period(1..5, run = 3)