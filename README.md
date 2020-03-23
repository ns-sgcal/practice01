# practice01
first practice

# code sample
```elisp
(defun insert-comment-char-to-tabstop ()
  (interactive)
  (insert
   (make-string (- 60 (current-column)) (string-to-char comment-start)))
)
(global-set-key "\C-c/" 'insert-comment-char-to-tabstop)
(add-hook 'text-mode-hook
          '(lambda ()
             (make-local-variable 'comment-start)
             (setq comment-start "#")))

```

# code sample 2

```elisp
(defun cb-copy ()
  (interactive)
  (let ((coding-system-for-write 'utf-8))
    (shell-command-on-region (region-beginning) (region-end) "cat > /dev/clipboard" nil nil nil))
  (message ""))
```


