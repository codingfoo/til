# Devops

Operations means delivering the app to the customer.
Operations is creating the software artifact

docker
vagrant
amis
capistrano

Embracing change

3 Basics:
Hosting account
Code repo
Data backup

dev ops with hot fail overs only failover one direction and not the other


immutable infrastructure - never patch a system, just replace

if you build it you run it
if you build it you secure it - provide support and training

gain visibilty into security of continually deployed/changing services/software


 In general, we try to align our downtime with our customers' downtime. At the end of the day, you have to pick a final failure point, and it's best if that can align with your customers' failure points as well. Namely, we're relying heavily on Amazon's ELB and the .com registrar to be up and functioning at all times, and we like this tradeoff because if the .com registrar or ELB is down, the whole internet is pretty much coming down with it. If our customers' sites are down, their email deliverability and event triggering is seemingly the last of their worries, so we're betting on the same infrastructure they are to align our incentives and lessen the impact of us having downtime issues.

On the human side of things, we have great rapport with them through our support efforts each and every day. This functions much like an insurance policy when we have unscheduled downtime or emergency maintenance. On the whole, a great strategy for lessening the impact of downtime is to make the uptime situation the best it can possibly be for the customer.



single point of deploy failure - 3rd party depencies - github, rubygems



docker
docker daemon
docker client
docker repo

process in a box, with everything
container starts and stops with program

make changes, docker file or running commands

image
  id
container
  id

commit


ids shas
labels


image
container instance of an image


can i install base images that are different than running host os?


code changes
ops/infrasturcture changes

abstract away underlying host
repeatability


data only volumes
move from one host to another
share common stuff between containiers(dry)

run tests in parallel by bring up seperate instances of the database



benefits of full vms
full isolation
resource gaurantees

containers: kernel shared
vms: kernel can be different


consistency: if completed / done for everyone
availability: may show up at different times for people but will always be up to date

because if so how diff than partition tolerance, availability is about the connections to cliens partition tolerance is about conections in the cluster



AWS
===
three types or permissions
1. user-based policy
2. resource based
3. resource level

blacklist does not work because new stuff is added


compartmentalization
who(or what) can apply(or delete) tags: escalate priviliges by adding tags

account level separation: prod vs test, segregate on different, front end
use multiple aws accounts
segeragate by billing boundries


different az are mapped differently in different accounts


monitoring aws security
aws cloudtrail - security and help you with handling api throttling

vpc's let you add more security groups and change on the fly

aws ec2 user data, a script that can be passed in and run on an instance during loading


SSL
===
SSL and nginx: https://docs.google.com/presentation/d/10iszJMl_WOJnfzdWal4NGHg-O6tcigxde2KY_F-yREc/present#slide=id.g3ee749ff2_0371


ansible
=======
  ad-hoc
  playbook system
    ansible-playbook <playbook> -e <extra env vars>

  host inventory
    groups - groups of groups
    can be from files, folder and files, queried from api

  connections
    local - api calls
    ssh - remote calls

  playbooks > plays
    plays > tasks
      tasks > modules

      handlers - tasks that can be called multiple times but are run once(ie webservers restart)

  name
  hosts
  vars
  tasks
  handlers

  vars
    playbooks
    command line -e flag
    discovered variables -> facts

  playbook dir structure
    files
    handlers
    tasks
    templates

  with_items
