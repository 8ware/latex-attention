* Detect multiple unnecessary usages by checking counters if greater 1
* Extend concept to also observe references from the text, i.e. wrap also
  `\ref` etc. to ensure that each figure etc. is described at least once in
  the text.
* Use the `\AtDocumentEnd` macro to print summary at the end.
* Maybe use auxiliary file to track usages.
* Move waring messages to macro, e.g.
	```
	\newcommand{\attention@msg@nocaption}{Missing caption!}
	```
* Warn if label before caption, e.g.
	```latex
	\begin{figure}
		...
		\label{fig:1}
		\caption{bla}
	\end{figure}
	```
  Currently this constellation is not detected since the checks are made after
  both macros were used, i.e. within the `\end{figure}` part. To detect that
  situation the check must be done within the `\label` command.
* Add options to exclude `figure[*]`, `table[*]` etc.
