# Scheduling Constraint Catalog

Each constraint should eventually document:

- ID;
- name;
- description;
- type;
- priority/weight;
- required inputs;
- satisfaction criteria.

## Hard Constraints

### HC-001 — Teacher collision

A teacher cannot teach more than one lesson in the same timeslot.

### HC-002 — Room collision

A room cannot host more than one class group in the same timeslot.

### HC-003 — Class group collision

A class group cannot attend more than one lesson in the same timeslot.

### HC-004 — Teacher availability

A teacher may only be scheduled in timeslots in which they are available.

### HC-005 — Teacher qualification

A teacher must be qualified to teach the assigned subject.

### HC-006 — Room capacity

The selected room must have capacity greater than or equal to the class group's student count.

### HC-007 — Curriculum workload

The generated schedule must satisfy the required number of weekly periods for each class group and subject.

## Soft Constraints

### SC-001 — Teacher subject preference

Prefer assigning subjects that teachers rate more highly.

### SC-002 — Minimize teacher gaps

Reduce idle periods between a teacher's lessons.

### SC-003 — Weekly distribution

Avoid concentrating all periods of a subject on too few days.

### SC-004 — Preferred timeslots

Prefer timeslots marked as desirable by the teacher.

### SC-005 — Room stability

Reduce unnecessary room changes when possible.

### SC-006 — Consecutive periods

Allow the model to reward or discourage consecutive periods of the same subject depending on configuration.

## Initial solver spike scope

Sprint 0 only needs to prove:

- HC-001;
- HC-002;
- HC-003;
- HC-004.

Later iterations can introduce the remaining constraints and scoring weights.
