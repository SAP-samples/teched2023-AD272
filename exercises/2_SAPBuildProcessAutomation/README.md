# Level 1 Heading

In this exercise, you will configure a SAP Build Process Automation project which can trigger an approval process for the mitigation proposed for the risk in the Risk Managment Build Apps application.

## Level 2 Heading

After completing these steps you will have learnt the following.

1)	Save as New Project
2)	Configure the decision with approver
3)	Import UI5 Form
4)	Add UI5 Form to Process 
5)	Add Action based on CAP Service
6)	Release and Deploy
7)	Test Process
   
<br>![](/exercises/ex0/images/00_00_0010.png)

2.	Insert this code.
``` abap
 DATA(params) = request->get_form_fields(  ).
 READ TABLE params REFERENCE INTO DATA(param) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.
```

## Summary

Now that you have ... 
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)
