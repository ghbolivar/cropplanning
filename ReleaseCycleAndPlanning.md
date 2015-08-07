# Issues #

There are three primary issue _tags_ which can help us to juggle all of the issues:

  * Version
  * Milestone
  * Priority

### Version ###

All issues **must have** a _Version_ label.  If a specific targeted version cannot be decided upon, then it should be labeled as _Future_.

### Milestone ###

_Milestone_ helps to qualify where in the release cycle each issue fits: Alpha, Beta or RC (Release Candidate)

_Milestone_ should only be specified if _Version_ is given as a specific number or release (ie 1.0, 1.5, etc.).  If _Version_ is specified as _Future_, then _Milestone_ **should be left blank** or unspecified.

### Priority ###

_Priority_ helps us judge how important an issue is.  It may be left unspecified if the _Version_ is _Future_.  Otherwise, the priorities are:

  * Blocking: of vital importance; the release cannot proceed w/o it; in an old release, the bug must be fixed immediately
  * Wanted: normal priority; highly desirable fixes/features, but a release can proceed w/o a fix
  * WouldBeNice: lowest priority; it would be great if we could handle these issues for the targeted release, but we can't make any guarantees