```
$ npx shadow-cljs clj-repl -A:shadow-cljs
shadow-cljs - config: /home/alex/repos/invalid-number-uuid-repro/shadow-cljs.edn
shadow-cljs - starting via "clojure"
shadow-cljs - server version: 2.19.5 running at http://localhost:9630
shadow-cljs - nREPL server started on port 41529
shadow-cljs - REPL - see (help)
To quit, type: :repl/quit
shadow.user=> (identity #uuid "0eb537e1-72bc-4d1a-89e0-8e3c2a7f8978")
#uuid "0eb537e1-72bc-4d1a-89e0-8e3c2a7f8978"
shadow.user=> (require '[meander.epsilon :as m])
Reflection warning, meander/util/epsilon.cljc:758:24 - reference to field val can't be resolved.
nil
shadow.user=> (identity #uuid "0eb537e1-72bc-4d1a-89e0-8e3c2a7f8978")
Execution error (NumberFormatException) at shadow.user$eval36931/<clinit> (REPL:3).
Invalid number: 0eb537e1-72bc-4d1a-89e0-8e3c2a7f8978
shadow.user=>
```
