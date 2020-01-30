SELECT o.Name as TableName,

i.rowcnt Row_count,

c.Name as ColumnName,

t.name as DataType,

t.length as [DataLength],

c.collation

FROM sysobjects o

JOIN syscolumns c

ON o.id = c.id

JOIN systypes t

ON c.xtype = t.xtype

JOIN Sysindexes i

ON o.id=i.id

WHERE o.xtype = 'u'

and i.indid in (0,1)

ORDER By o.name

-- References
-- https://www.sqlservercentral.com/forums/topic/how-can-i-export-all-table-names-plus-column-names-from-sql
