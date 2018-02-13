Talking about 7 years about topic

not only requirements - requirements in ecosystem
everything changes all the time
Evolutionary arch support GUIDED, INCREMENTAL changes across MULTIPLE DIMENSIONS

You cannot increment security and performance in the same time. You need to choice

# Evolutionary computing fitness function
- Assesment of architecture
- Addition to metrics and tests

## Ingredients
### Atomic
run agains single context
ex: Monitoring 

### Holistic
run against shared context and check it in group
ex. Chaos Monkey

### Triggered 
Run one time
Triggered functions are in majority holistic
ex: Monitoring 

### Continouse
Running all the time
ex. Logging
ex. Chaos Monkey

### Static
Has a fixed result - binary pass, fail
### Dynamic
Has not binary result 

### Automated
Tests and other mechanism
### Manual
Must involve humans

### Temporal
You can fe. break on upgrade if there is new version, you can do this after fe. 2 months
### Domain specific
Security or Regulatory

### Intentional 
Known from the start of project
### Emergent
Emerged during process of development

## Examples

### Cyclic Dependency Function
jdepend - https://github.com/clarkware/jdepend 
Put it in the build to be sure you are checking over it all the time

### Consumer Driven Contracts
We do tests, now we can do whatever we want until tests fails

- System-Wide Fitness Function
- Invidual Fitness Functions 

We cannot have just definition, we need to have way of verification


### Incremental - small scale changes
- Functionality - create new service - make it better  - people started moving to it - desintegrate when everybody resign from it

- Deployment pipelines

if we have incremental changes, we can change also our Fitness Function in the incremental way
1. Identify dimension affected by evolution
2. Define fitness function for each dimension
3. Use deployment pipelines to automate fitness function




## Multiple Dimensions - don't focus on only one dimension, focus on all
- Auditibility
- Performance
- Security
- Data
- Legality
- Scalability

You cannot do conscious decision if your teams cluseter ex. Security
