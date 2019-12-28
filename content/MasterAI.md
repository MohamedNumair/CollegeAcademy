# Artificial Intelligence

Class: Electrical, Electrical Master
Created: Dec 10, 2019 10:09 AM
Reviewed: No

# Contents

# Overview

## Dr. Abdellsalam

- Lec 1: Fuzzy Chapter:  Introduction
- Lec 2: Fuzzy Chapter: Methods and Examples
- Lec 3: Fuzzy Chapter: Speed Response
- Lec 4: Fuzzy Chapter: Wind
- Lec 5: Research papers:
- Lec 6: Research papers:

## Dr. Refaat

- Lec 7: Neural Network
- Lec 8: Neural Network Training
- Lec 9: Genetic Algorithm
- Lec 10: Genetic Algorithm

# Fuzzy

- What is fuzzy logic (FL)?

    class of AI, Based on the nature of fuzzy human thinking, deals with problems that have fuzziness or vagueness, defined as multi-valued logic (0 to I), deals with imprecise information

- What's a fuzzy set?

    fuzzy set (fuzzy value) theory based on FL, a particular object has a degree of membership in a given set that
    may be anywhere in the range of O (completely not in the set) to 1 (completely in the set)

- What's a Fuzzy problem ?

    an input/output, static, nonlinear mapping problem through a "black box," as
    shown, all the input information is defined in the input space, it is processed in
    the black box, and the solution appears in the output space.

    ![Artificial%20Intelligence/Untitled.png](Artificial%20Intelligence/Untitled.png)

    - mapping can be static or dynamic, and the mapping characteristics are determined by the black box's characteristics.
    - The black box cannot only be a fuzzy system, but also an ES, neural network, general mathematical system, such as differential equations, algebraic equations, etc., or anything else.
- What's a Membership Function? give examples .

    An MF is a curve that defines how the values of a fuzzy variable in a certain
    region are mapped to a membership valueμ ( or degree of membership) between 0 and I.

    ![Artificial%20Intelligence/Untitled%201.png](Artificial%20Intelligence/Untitled%201.png)

    ![Artificial%20Intelligence/Untitled%202.png](Artificial%20Intelligence/Untitled%202.png)

    ![Artificial%20Intelligence/Untitled%203.png](Artificial%20Intelligence/Untitled%203.png)

- What are the possible operations on fuzzy ? what are its properties ?

    ## Operatoins

    AND :  max ( A,B)

    OR :   min ( A,B)

    NOT : NOT(A)=  1-(A)

    Product : (same x axis ) multiply MFs

    Power : raise MF to power of m( positive)

    ![Artificial%20Intelligence/Untitled%204.png](Artificial%20Intelligence/Untitled%204.png)

    ## Properties :

    ![Artificial%20Intelligence/Untitled%205.png](Artificial%20Intelligence/Untitled%205.png)

    ![Artificial%20Intelligence/Untitled%206.png](Artificial%20Intelligence/Untitled%206.png)

- What does a fuzzy inference problem consist of ?

    • Step l: Fuzzification of input variables
    • Step 2: Application of fuzzy operator (AND, OR, NOT) in the IF (antecedent) part of the rule
    • Step 3: Implication from the antecedent to the consequent (THEN part of the rule)
    • Step 4: Aggregation of the consequents across the rules
    • Step 5: Defuzzification

    ![Artificial%20Intelligence/Untitled%207.png](Artificial%20Intelligence/Untitled%207.png)

    ![Artificial%20Intelligence/Untitled%208.png](Artificial%20Intelligence/Untitled%208.png)

- Mention some of the **implication methods** used in FL.

    ## Mamdani Type

    ![Artificial%20Intelligence/Untitled%209.png](Artificial%20Intelligence/Untitled%209.png)

    ## Lusing Larson Type

    ![Artificial%20Intelligence/Untitled%2010.png](Artificial%20Intelligence/Untitled%2010.png)

    ## Sugeno Type

    ### Singleton (zero-order)

    rules states a K 

    ![Artificial%20Intelligence/Untitled%2011.png](Artificial%20Intelligence/Untitled%2011.png)

    ![Artificial%20Intelligence/Untitled%2012.png](Artificial%20Intelligence/Untitled%2012.png)

    ### first-order

    rules state operands

    ![Artificial%20Intelligence/Untitled%2013.png](Artificial%20Intelligence/Untitled%2013.png)

    each rule as defining the location of a moving singleton. that is. the singleton output spikes can move around in a linear fashion in the output space depending on the input signal values

    ![Artificial%20Intelligence/Untitled%2014.png](Artificial%20Intelligence/Untitled%2014.png)

    Fuzzy model on DC Machine

- What's defuzzifaction? mention its methods.

    it's the conversion of the fuzzy output ( the aggregated union of the fired rules output) into a crisp output

    its methods are :

    1. Center of Area (COA) method [ centre of gravity]

    $$Z_{0} = \frac{\int {Z.\mu_{out}(Z)}}{\int {\mu_{out}(Z)}dz}$$

    discrete :

    $$Z_{0} = \frac{\sum_{i=1}^{n}{Z.\mu_{out}(Z)}}{\sum_{i=1}^{n} {\mu_{out}(Z)}dz}$$

    Ex: 

    ![Artificial%20Intelligence/Untitled%2015.png](Artificial%20Intelligence/Untitled%2015.png)

    ![Artificial%20Intelligence/Untitled%2016.png](Artificial%20Intelligence/Untitled%2016.png)

    2. Height Method

    COA but consider only the height of each contributing MF at the mid-point of the base.

    ![Artificial%20Intelligence/Untitled%2017.png](Artificial%20Intelligence/Untitled%2017.png)

    3. Mean of Maxima (MOM) Method 

    takes only the z of the highest MF (for above example Z0= 3 )

    for m number of MFs that have the same height take the average

    4. Sugeno Method

    zero order

    ![Artificial%20Intelligence/Untitled%2018.png](Artificial%20Intelligence/Untitled%2018.png)

    first order

    ![Artificial%20Intelligence/Untitled%2019.png](Artificial%20Intelligence/Untitled%2019.png)

- What's Fuzzy Control (FC)?

    Fuzzy control is basically an adaptive and nonlinear
    control, which gives robust performance for a linear or nonlinear plant with parameter variation

- How to implement a P, PI and PID control in fuzzy?

    only by using the E error and CE change of error signals we can use 

    ## P control

    as example rule: IF E = positive small (PS) THEN U = positive big (PB)

    so, only kp  = K and KE=U

    ## PI Control

    Rule I: IF E = ZE AND CE= NS THEN DU= NS
    Rule 2: IFE= PS AND CE= NS THEN DU= ZE

    ![Artificial%20Intelligence/Untitled%2020.png](Artificial%20Intelligence/Untitled%2020.png)

    and to get U we integrate or sum

    ![Artificial%20Intelligence/Untitled%2021.png](Artificial%20Intelligence/Untitled%2021.png)

    so,

    ![Artificial%20Intelligence/Untitled%2022.png](Artificial%20Intelligence/Untitled%2022.png)

    ## PID Controller

    example rule: IF E = PS AND CE= NS AND e' E = PS THEN DU= ZE,

    ![Artificial%20Intelligence/Untitled%2023.png](Artificial%20Intelligence/Untitled%2023.png)

- Draw a general fuzzy control block diagram, with the general structure of a fuzzy feedback control system.

    in control of the speed in induction machine (VC based)

    ![Artificial%20Intelligence/Untitled%2024.png](Artificial%20Intelligence/Untitled%2024.png)

     the general structure of a fuzzy feedback control system

    ![Artificial%20Intelligence/Untitled%2025.png](Artificial%20Intelligence/Untitled%2025.png)

- What are the available control implementation methods for fuzzy control ?
    1. Using real time computation (C program, FL Toolbox or DSP ASIC chips)
    2. Using a look up table where all computation are done a head in hierarchical tables (coarse, medium and fine)

- What is the fuzzy logic control design methodology?
    1. Analyze if the problem requires FC ?
    2. get design info and experience from operator.
    3. if plant model available simulate it and study its characteristics.
    4. identify functional elements where to apply FL.
    5. identify the inputs and outputs of each fuzzy sys.
    6. define universe of discourse and convert to pu values.
    7. formulate fuzzy sets, choose MF shapes
        - sensitive : need more fuzzy sets
        - more precision near S.S : crowding of MFs near the origin
    8. formulate rule table.
    9. if there is a plant model , test and iterate fuzzy sets and rules

        if not available, design a conservative fuzzy control and test on plant operation.

    10. implement in real time, and iterate to improve performance

- Mention some of fuzzy logic control applications in power electronic systems.

    Applications include
    1. speed control of dc and ac drives

    2. feedback control of converter
    3. off-line P-I and P-I-D tuning.
    4. nonlinearity compensation
    5. on-line and off-line diagnostics
    6. modeling
    7. parameter estimation.
    8. performance optimization of drive systems based on on-line search
    9. estimation for distorted waves

- Draw the fuzzy MFs for induction motor speed control.

    ![Artificial%20Intelligence/Untitled%2026.png](Artificial%20Intelligence/Untitled%2026.png)

    ![Artificial%20Intelligence/Untitled%2027.png](Artificial%20Intelligence/Untitled%2027.png)

- write down a rule matrix for fuzzy speed control

    ![Artificial%20Intelligence/Untitled%2028.png](Artificial%20Intelligence/Untitled%2028.png)

    ![Artificial%20Intelligence/Untitled%2029.png](Artificial%20Intelligence/Untitled%2029.png)

- draw the typical speed response with stepped load torque TL, and then show a similar response with four times the rotor inertia, comment.

    ![Artificial%20Intelligence/Untitled%2030.png](Artificial%20Intelligence/Untitled%2030.png)

    ![Artificial%20Intelligence/Untitled%2031.png](Artificial%20Intelligence/Untitled%2031.png)

    The performances are superior to conventional PI control. The robustness in the response is evident from the results., with more inertia it took more time to get to ss but it did due to robustness of the controller and parameter variation (inertia) didn't affect its response not mentioning its stability.

- 

[Speed control of DC motor using Fuzzy Logic Controller.zip](Artificial%20Intelligence/Speed_control_of_DC_motor_using_Fuzzy_Logic_Controller.zip)

# Artificial Neural Networks

# Genetic Algorithm

- What's Genetic Algorithm ?
    - a **search technique** used in computing to find true or approximate solutions to optimization and search problem.
    - **global** search heuristics
    - class of evolutionary algorithms that use techniques inspired by evolutionary biology such as **inheritance**, **mutation**, **selection**, and **crossover** (recombination)
    - **probabilistic intelligent search** algorithm, which searches a population of points in parallel.
- In what does GA differ from other optimization techniques ?

    •	It searches a population of points in **parallel**
    •	It uses **probabilistic** rules rather than deterministic ones
    •	It can process an **encoding** set of parameters

- Give an overview of the evolution process in GA.
    1. starting from a population of **randomly** generated individuals
    2. then evolution happens in generations
    3. In each generation, the fitness of every individual in the population is evaluated
    4. multiple individuals are selected from the current population (based on their fitness)
    5. the selected individual are modified to form a new population.
    6. new population is used in the next iteration of the algorithm
    7. To terminate algorithm either 1) a max. number of generations 2) satisfactory fitness level acquired.

    •	Start with a large “population” of randomly generated “attempted solutions” to a problem
    •	Repeatedly do the following:
    	Evaluate each of the attempted solutions
    	(probabilistically) keep a subset of the best solutions
    	Use these solutions to generate a new population
    •	Quit when you have a satisfactory solution (or you run out of time)

- Define, individual, Population and Fitness.

    Population : Group of all individuals Target (search space)

    Individual : Any possible solution also called chromosome

    Fitness : function that we optimize (each individual has a fitness)

- What's penalty cost ?

    To initiate the population, a number of individuals are randomly formulated in the range of variables
    Each individual in the randomly-created population is tested for violating the constraints
    If the solution is infeasible, a suitable additional penalty cost is assigned to the individual
    The performance of each individual is evaluated by calculating the value of **objective function** and adding the corresponding penalty term if exists

- What's individuals fitness value ?
    - The individuals are ranked depending on their corresponding costs and a suitable fitness value is assigned to each one
    - The fitness values could be calculated depending on the position of the individuals within the population rather than their distinct performance
    - Fitness values between maximum and minimum limits are calculated with fixed incremental steps and assigned to the ranked individuals
- Use a random population pool to represent the GA steps.

    ![Artificial%20Intelligence/Untitled%2032.png](Artificial%20Intelligence/Untitled%2032.png)

    ![Artificial%20Intelligence/Untitled%2033.png](Artificial%20Intelligence/Untitled%2033.png)

- What's the Constraints representation problem in GA ? and what are the approaches to solve this problem ?
    - To employ GA with a tightly-constrained problem, it is possible to generate only feasible solutions by avoiding individuals which violate the given constraints
    - but, the infeasible solutions mostly cover the search space at the initial generation, so the avoidance will cause missing the area of global minimum

    **Approaches**,

    1. Move the infeasible individuals to the nearest feasible area,
        - but this would be too complex and a very time consuming
    2. Penalty function convert to an unconstrained problem by augmenting additional cost terms with the main objective function
    - nonlinear costs for solutions that violate the constraints depending on their relative locations with respect to the feasibility boundaries
    - ensure adequate choice of the penalty functions and their parameters for rapid rejection
    - differentiate in performance between the infeasible individuals themselves, which will help in the evolution process
    - higher cost value has to be assigned to any infeasible solution than the feasible members, for fast rejection

- Draw a flowchart defining the GA search algorithm.

    ![Artificial%20Intelligence/Untitled%2034.png](Artificial%20Intelligence/Untitled%2034.png)

- What's crossover?

    Crossover is a genetic process to exchange information between members of the population.

    It's the generation of new individuals of the next generation by mating parents by choosing a crossover point 

    ![Artificial%20Intelligence/Untitled%2035.png](Artificial%20Intelligence/Untitled%2035.png)

    or can be a two point cross over to mate the middle part genes, avoiding genes at the beginning and end of chromosome

    ![Artificial%20Intelligence/Untitled%2036.png](Artificial%20Intelligence/Untitled%2036.png)

    or can be by choosing random subset from one parent and replacing it from the another parent.

    ![Artificial%20Intelligence/Untitled%2037.png](Artificial%20Intelligence/Untitled%2037.png)

- What's Mutation?

    it's small disruptive change in the new generation members

    ![Artificial%20Intelligence/Untitled%2038.png](Artificial%20Intelligence/Untitled%2038.png)

- Suppose we want to maximize the number of ones in a string of (L) binary digits
An individual is encoded (naturally) as a string of l binary digits
The fitness (f) of a candidate solution is the number of ones in its genetic code

    We start with a population of “n” random strings. Suppose that L= 10 and n= 6

    1. We toss a fair coin 60 times and get the following initial population:

    ![Artificial%20Intelligence/Untitled%2039.png](Artificial%20Intelligence/Untitled%2039.png)

    2. We randomly select a subset of the individuals based on their fitness according to

    $$Pie \ Section = \frac{f(i)}{\sum_{i}^{n}{f(i)}}$$

    ![Artificial%20Intelligence/Untitled%2040.png](Artificial%20Intelligence/Untitled%2040.png)

    3. Suppose that, after performing selection, we get the following population::

    ![Artificial%20Intelligence/Untitled%2041.png](Artificial%20Intelligence/Untitled%2041.png)

    4. we choose 0.6 of the 6 chosen to perform crossover, choose random two point cross over

    ![Artificial%20Intelligence/Untitled%2042.png](Artificial%20Intelligence/Untitled%2042.png)

    5. after crossover we get new 0.6*6 = 4 individuals (initial strings in the next photo) 

    6. these 4 new individuals we allow for 0.1 mutation (one bit) 

    ![Artificial%20Intelligence/Untitled%2043.png](Artificial%20Intelligence/Untitled%2043.png)

    And now, iterate …
    In one generation, the total population fitness changed from 34 to 37, thus improved by ~9%
    At this point, we go through the same process all over again, until a stopping criterion is met

- What are selection methods in GA?
    1. Roulette wheel (one pointer)

    ![Artificial%20Intelligence/Untitled%2040.png](Artificial%20Intelligence/Untitled%2040.png)

    you will need N rolls to get N solutions

    2. N equally space pointers 

    ![Artificial%20Intelligence/Untitled%2044.png](Artificial%20Intelligence/Untitled%2044.png)

    one roll will give you N solution

- How to do recombination in non-binary chromosomes ?

    ### Crossover

    Crossover is a genetic process to exchange information between members of the population.

    For the real-valued encoding, the max-min arithmetical crossover operator can be used as follows

    ![Artificial%20Intelligence/Untitled%2045.png](Artificial%20Intelligence/Untitled%2045.png)

    ### Mutation

    It is the second process in the recombination, which is used to escape from possible local minima.
    The mutation in the real-coded representations is accomplished by disturbing the *gene values with low probability*.

- What's Elitism?
    - to ensure that the best solutions are not lost in moving from one generation to the next.
    - some of the fittest members of each generation are saved and copied into the next generation.
    - the average fitness of the new generation is improved.
- Give a numerical example of a GA problem parameters

    ### Number of individuals per subpopulation  (20)

    *for migration purposes.*

    ### Total population size                                   (200)

    *the number of individuals* 

    ### Generation gap                                           (0.8)

    *number of individuals recombination are made on*

    ### Insertion rate                                              (0.9)

    *that 0.9 of the new generation will replace the worst same number of individuals in the old generation*

    ### Probability of mutation                             (0.01)

    *how much of the genes will be mutated*

    ### Maximum generations                              (1000)

    *the number of generation at which the algorithm terminates*

- We want to construct a box whose base length is 3 times the base width. The material used to build the top and bottom cost $10/ft2 and the material used to build the sides cost $6/ft2. If the box must have a volume of 50ft3 determine the dimensions that will minimize the cost to build the box

    ![Artificial%20Intelligence/Untitled%2046.png](Artificial%20Intelligence/Untitled%2046.png)

    ![Artificial%20Intelligence/Untitled%2047.png](Artificial%20Intelligence/Untitled%2047.png)
