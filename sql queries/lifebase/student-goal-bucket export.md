
```
select  
    s.id StudentId,  
    concat_ws(' ', s.first_name, s.last_name) Student,  
    sg.id DoelId,  
    sg.title Doel,  
    b.id PvaId,  
    b.name pva,  
    count(DISTINCT(ba.id)) ActieCount,  
    group_concat(DISTINCT(ba.name) ORDER by ba.sequence SEPARATOR ', ')  
from student_goal sg  
left join bucket b on b.student_goal_id = sg.id  
join student s on s.id = sg.student_id  
join group_student gs on gs.student_id = s.id  
join `group` g on g.id = gs.group_id  
join bucket_action ba on ba.bucket_id = b.id  
where g.id in (164, 177)  
and sg.title NOT IN ("Algemene ontwikkeling", "Horizonverbreding")  
group by s.id, sg.id, b.id  
order by s.id asc;
```

---
pascal maandag 177
pascal woensdag 164

zuiderzee 163

hlw donderdag 151
hlw dinsdag 152

lely lyceum 159

#lifebase