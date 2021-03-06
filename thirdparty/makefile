# Examples:
#  $ make MAIN=FileSorter ARG=. 

N := 3
MAIN := HelloWorld
ARG := 1Kints.txt

ALGS4SRC ?= .

# $ javac-algs4.bat -cp ./algs4.jar ThreeSum.java Stopwatch.java

JC  := javac-algs4.bat
JVM := java-algs4.bat
#JC  := javac
#JVM := java
CHK := checkstyle-algs4.bat
BUG := findbugs-algs4.bat
#JFLAGS := -Xlint:unchecked -cp ./algs4.jar
#JFLAGS := -cp ./algs4.jar
.PHONY: clean

SRCS = \
  FileSorter.java \
  HelloWorld.java \
  Merge.java \
  MergeBU.java \
  MergeX.java \
  Selection.java \
  Stopwatch.java \
  ThreeSum.java  
# StdArrayIO.java \
# StdDraw.java \
# StdIn.java \
# StdOut.java \
# StdRandom.java \
# StdStats.java \
# Bag.java \
# BinarySearch.java \
# BouncingBalls.java \
# BST.java \
# Date.java \
# EvaluatePostfix.java \
# GrahamScan.java \
# Heap.java \
# Insertion.java \
# Knuth.java \
# LinkedBag.java \
# LinkedQueue.java \
# LinkedStack.java \
# MaxPQ.java \
# MinPQ.java \
# Point2D.java \
# Queue.java \
# Quick.java \
# Quick3way.java \
# QuickFindUF.java \
# QuickUnionUF.java \
# QuickX.java \
# ResizingArrayBag.java \
# ResizingArrayQueue.java \
# ResizingArrayStack.java \
# Shell.java \
# ST.java \
# Stack.java \
# ThreeSumFast.java \
# UnorderedMaxPQ.java \
# WeightedQuickUnionUF.java

# If needed, clear any default definitions for these targets
.SUFFIXES: .java .class

# --------------------------------------------------------------
# Targets

runa: $(MAIN).class 
	$(JVM) $(JFLAGS) $(MAIN) $(ARG)

run: $(MAIN).class 
	$(JVM) $(JFLAGS) $(MAIN) 

# 'class' is the suffix of the target file
# 'java' is the suffix for the dependency file
# i.e. If MAIN.java source changes, re-compile MAIN.class
.java.class:
	$(JC) $(JFLAGS) $(SRCS)


# WordNet
algs2_1: 
	echo "WordNet"

# Content-Aware Resizing
algs2_2: 
	echo "Content-Aware Resizing"

# Baseball Elimination
algs2_3: 
	echo "Baseball Elimination"

# Boggle
algs2_4: 
	echo "Boggle"

# Burrows-Wheeler algorithm
algs2_5: 
	echo "Burrows-Wheeler algorithm"

# Algs1 Week 1 Programming Assignment 
wk1: Percolation.class PercolationStats.class
	$(JVM) PercolationStats 10 2

wk1_chk:
	$(CHK) Percolation.java PercolationStats.java

wk1_zip:
	zip percolation.zip Percolation.java PercolationStats.java

# Algs1 Week 2 Programming Assignment 
wk2: Deque.class RandomizedQueue.class Subset.class 
	$(JVM) Subset $(N)

wk2a: RandomizedQueue.class test_RandomizedQueue.class
	$(JVM) test_RandomizedQueue $(N)

wk2_zip:
	zip queues.zip Deque.java RandomizedQueue.java Subset.java


# Algs1 Week 3 Programming Assignment 
wk3a: LineSegment.class Point.class BruteCollinearPoints.class FastCollinearPoints.class
	$(JVM) BruteCollinearPoints $(N)

wk3b: LineSegment.class Point.class BruteCollinearPoints.class FastCollinearPoints.class
	$(JVM) FastCollinearPoints $(N)

wk3_zip:
	zip collinear.zip Point.java BruteCollinearPoints.java FastCollinearPoints.java


wk4: Board.class Solver.class
	$(JVM) Solver

wk4_zip:
	zip 8puzzle.zip Board.java Solver.java


wk5_zip:
	zip kdtree.zip PointSET.java KdTree.java


wordnet.zip: SAP.java WordNet.java Outcast.java
	zip $@ $<

seamCarving.zip: SeamCarver.java
	zip $@ $<

baseball.zip: BaseballElimination.java 
	zip $@ $<

# A4 BoggleSolver.java, along with any other supporting files (excluding BoggleBoard.java and algs4.jar).
boggle.zip: BoggleSolver.java
	zip $@ $<

burrows.zip: MoveToFront.java BurrowsWheeler.java CircularSuffixArray.java
	zip $@ $<


Percolation.class: $(ALGS4SRC)/Percolation.java
	$(JC) -d . $<

PercolationStats.class: $(ALGS4SRC)/PercolationStats.java
	$(JC) -d . $<


Deque.class: $(ALGS4SRC)/Deque.java
	$(JC) -d . $<

RandomizedQueue.class: $(ALGS4SRC)/RandomizedQueue.java
	$(JC) -d . $<

test_RandomizedQueue.class: test_RandomizedQueue.java
	$(JC) -d . $<

Subset.class: $(ALGS4SRC)/Subset.java
	$(JC) -d . $<


Point.class: $(ALGS4SRC)/Point.java
	$(JC) -d . $<

BruteCollinearPoints.class: $(ALGS4SRC)/BruteCollinearPoints.java
	$(JC) -d . $<

FastCollinearPoints.class: $(ALGS4SRC)/FastCollinearPoints.java
	$(JC) -d . $<


LineSegment.class: $(ALGS4SRC)/LineSegment.java
	$(JC) -d . $<

Board.class: $(ALGS4SRC)/Board.java
	$(JC) -d . $<

Solver.class: $(ALGS4SRC)/Solver.java
	$(JC) -d . $<


PointSET.class: $(ALGS4SRC)/PointSET.java
	$(JC) -d . $<

KdTree.class: $(ALGS4SRC)/KdTree.java
	$(JC) -d . $<


clean:
	rm -f *.class
	rm -f *.zip

