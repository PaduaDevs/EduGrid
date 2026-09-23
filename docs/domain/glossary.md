# EduGrid Domain Glossary

This document defines the initial shared vocabulary for EduGrid.

## Institution

An educational institution whose scheduling data is managed by EduGrid.

## Teacher

A professional who may be assigned to teach one or more subjects. A teacher has availability, workload limits, qualifications, and preferences.

## Subject

An academic subject such as Mathematics, History, or Physics.

## TeacherSubject

Relationship between a teacher and a subject.

It separates two concepts:

- **qualification**: whether the teacher is allowed to teach the subject;
- **preference**: how desirable that subject is for the teacher.

## ClassGroup

A student group or class, such as "9th Grade A".

Typical attributes include:

- academic year;
- shift;
- student count.

## Room

A physical resource where a lesson can occur.

Typical attributes include:

- capacity;
- room type;
- availability.

## Timeslot

A discrete scheduling period, identified by weekday, start time, end time, and order.

## TeacherAvailability

Defines whether a teacher may be assigned to a specific timeslot.

Future versions may distinguish:

- unavailable;
- available;
- preferred.

## CurriculumRequirement

Defines how many weekly periods a class group requires for a subject.

Example:

> 9A requires 5 Mathematics periods per week.

## Schedule

A timetable being drafted, generated, validated, published, or archived.

## ScheduleAssignment

A concrete assignment connecting:

- class group;
- subject;
- teacher;
- room;
- timeslot.

Assignments may be locked to prevent the solver from moving them during regeneration.

## ScheduleRun

A recorded execution of the optimization engine.

It may store:

- start/end timestamps;
- status;
- solver version;
- score;
- metadata.

## Hard Constraint

A rule that must never be violated in a valid timetable.

## Soft Constraint

A preference used to score and compare valid timetables. Violating one does not make a timetable invalid.

## Lock

A user-controlled flag indicating that an assignment must remain unchanged during subsequent solver runs.
