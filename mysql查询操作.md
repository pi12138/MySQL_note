# `MySQL查询`

## 多表查询

- 现在有三个表，`guardians_guardian, guardians_guardianstudent, students_student`
- 表`guardians_guardianstudent`中有其他两个表的外键。

```mysql
SELECT guardians_guardian.id, guardians_guardian.name, guardians_guardian.avatar, students_student.id, students_student.fullname, guardians_guardianstudent.relation
FROM guardians_guardianstudent, guardians_guardian, students_student
WHERE guardians_guardianstudent.student_id = students_student.id and guardians_guardianstudent.guardian_id = guardians_guardian.id and guardians_guardian.id = 652; 
```

