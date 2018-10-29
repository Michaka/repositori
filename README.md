# 
(define generate-interval
  (lambda
      (start end)(
         if(> start end)
           '()
           (cons start (generate-interval (+ start 1) end))
      )
   )
)

(define zip
  (lambda
      (list_one list_two)
    (
     if(null? (cdr list_one))
       (cons (car list_one) (car list_two))
       (cons (cons (car list_one) (car list_two)) (zip (cdr list_one) (cdr list_two)))
       )
    )
  
