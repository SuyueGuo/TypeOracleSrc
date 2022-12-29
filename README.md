# TypeOracle: Operand-Variation-Oriented Differential Analysis for Fuzzing Binding Calls in PDF Readers

TypeOracle proposed a novel approach to extract observable features from the execution traces for inferring the parameter types of binding calls, then the inferred type information is used to guide the generation of test cases. TypeOracle detected 38 previously unknown bugs, 26 of which were certified with CVE numbers. 

This repository  includes three parts, type inference, fuzzer and coverage collecting.

For the type inference part, TypeOracle uses differential analysis to reason about the type information of the binding calls in PDF Readers.

For the fuzzer part, TypeOracle uses the type information to guide the generation of test PDFs.

For coverage collecting part, TypeOracle uses DynamoRIO to collect the coverage information when running test PDFs.



## Installation 

#### Platform

- Windows 8.1/ Windows 10 64bit
- Python3(pywinauto, psutil need to be installed)

#### Prerequisites

- Adobe Acrobat Reader (32bit, English version, installed in the default directory.)
- Foxit PDF Reader (32bit, English version, installed in the default directory.)



## how to reproduce

We have prepared very detailed guidance for the reproduction, you can find them from README.pdf along with the source code. Besides, we have also prepared these README files in the virtual machine.

For the type inference, please refer to `TypeInfer\adobe\README.pdf` for type inference in Adobe Reader and `TypeInfer\foxit\README.pdf` for type inference in Foxit Reader.

For the fuzzer , please refer to `Fuzzer\README.pdf`.

For the coverage collecting, please refer to `Coverage\README.pdf`.
