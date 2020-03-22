# practice01
first practice

# code sample
```elisp
(defun insert-comment-char-to-tabstop ()
  (interactive)
  (insert
   (make-string (- 60 (current-column)) ?/))
)
(global-set-key "\C-c/" 'insert-comment-char-to-tabstop)
(add-hook 'text-mode-hook
          '(lambda ()
             (make-local-variable 'comment-start)
             (setq comment-start "#")))

```



