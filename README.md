Artifact of paper:

  *Avoiding the Shoals - A New Approach to Liveness Checking*

'xxx' is the binary file of our implementation which is evaluated in the paper.

## Usage

### Algorithms:

rlive:
```
$ ./xxx -a rlive -sub_checker 1 -rlive-prune-dead 1 <AIGER_file.aig>
```
- -sub_checker: safe checker used (1: IC3, 2: Forward CAR, 3: Backward CAR)
- -rlive-prune-dead: enable the prune-dead optimization
---

k-Liveness:
```
$ ./xxx -a ic3 -fair 0 -klive 1 -klive-cex 1 <AIGER_file.aig> 
```
FAIR:
```
$ ./xxx -a fcar -fair 1 -klive 0 -fw 1 <AIGER_file.aig>
```
k-FAIR:
```
$ ./xxx -a bcar -fair 1 -klive 1 -fw 1 <AIGER_file.aig>
```
- -a: safe checker used (ic3, fcar, bcar)
- -fair: enable fair
- -klive: enable k-Liveness
- -klive-cex: enable k-Liveness to identify counterexamples
- -fw: enable wall constraints during fair/k-FAIR

## Benchmarks
http://fmv.jku.at/hwmcc15/hwmcc15-benchmarks-live.7z