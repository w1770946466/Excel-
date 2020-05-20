    
    import xlrd  
    #导入xlrd库
    
    xlsx = xlrd.open_workbook(r'd:\Users\samsung\Desktop\文本文档\数控作业\数控鉴定教材题库-单选.xls')
    #打开Excel文件位置

    table = xlsx.sheet_by_index(0)
    #打开Excel文件中的第一个表格  0代表第一个以此类推 

    for n in range(1,table.nrows): 

	    print(n,'、题目'+table.cell(n,1).value,sep='')

	    print('答案：'+table.cell(n,9).value)

	    print('***********************')

    #利用for循环读取第2列和第10列所有内容
    #注意 列数=表格上标注列数-1
    #即    1 = 0
    #行数同上.
    #table.nrows 整工作表中所有行
    #table.cell(1,2).value  读取表格中第（2,3）中的数据
  
