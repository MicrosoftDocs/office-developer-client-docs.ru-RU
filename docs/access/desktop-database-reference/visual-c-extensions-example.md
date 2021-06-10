---
title: Visual C++ Extensions Example
TOCTitle: Visual C++ Extensions Example
ms:assetid: fe57868f-5707-3c5b-cb93-4121732d67cc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250305(v=office.15)
ms:contentKeyID: 48548934
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 080281ae0deb25fa10fcdccd8577d3aab076c2cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312070"
---
# <a name="visual-c-extensions-example"></a>Пример расширений Visual C++


**Область применения**: Access 2013, Office 2013

В этой программе показано, как извлекаются значения из полей и преобразуются в переменные C/C++.

В этом примере также можно использовать "интеллектуальные указатели", которые автоматически обрабатывают сведения о вызове и подсчете ссылок для интерфейса **IADORecordBinding.**

Без интеллектуальных указателей можно кодировать:

```cpp 
 
IADORecordBinding *picRs = NULL; 
... 
TESTHR(pRs->QueryInterface( 
 __uuidof(IADORecordBinding), (LPVOID*)&picRs)); 
... 
if (picRs) picRs->Release(); 
```

С помощью интеллектуальных указателей вы получите тип IADORecordBindingPtr из типа интерфейса IADORecordBindBinding с этим утверждением:

```cpp 
 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
```

И мгновенно наберем указатель вот так:

```cpp 
 
IADORecordBindingPtr picRs(pRs); 
```

Так как расширения Visual C++ реализованы объектом **Recordset,** конструктор для умной указатель, picRs, принимает \_ указатель RecordsetPtr, pRs . Конструктор вызывает QueryInterface с помощью pRs, чтобы найти указатель \_ RecordsetPtr, pRs . Конструктор вызывает QueryInterface с помощью pRs для поиска интерфейса IADORecordBinding.

```cpp 
 
// Visual C++ Extensions Example 
#import "c:\Program Files\Common Files\System\ADO\msado15.dll" no_namespace rename("EOF", "EndOfFile") 
 
#include <stdio.h> 
#include <icrsint.h> 
_COM_SMARTPTR_TYPEDEF(IADORecordBinding, __uuidof(IADORecordBinding)); 
 
inline void TESTHR(HRESULT _hr) { if FAILED(_hr) _com_issue_error(_hr); } 
 
class CCustomRs : public CADORecordBinding 
{ 
BEGIN_ADO_BINDING(CCustomRs) 
 ADO_VARIABLE_LENGTH_ENTRY2(2, adVarChar, m_ch_fname, 
 sizeof(m_ch_fname), m_ul_fnameStatus, false) 
 ADO_VARIABLE_LENGTH_ENTRY2(4, adVarChar, m_ch_lname, 
 sizeof(m_ch_lname), m_ul_lnameStatus, false) 
END_ADO_BINDING() 
public: 
 CHAR m_ch_fname[22]; 
 CHAR m_ch_lname[32]; 
 ULONG m_ul_fnameStatus; 
 ULONG m_ul_lnameStatus; 
}; 
 
void main(void) 
{ 
 ::CoInitialize(NULL); 
 try 
 { 
 _RecordsetPtr pRs("ADODB.Recordset"); 
 CCustomRs rs; 
 IADORecordBindingPtr picRs(pRs); 
 
 pRs->Open("SELECT * FROM Employee ORDER BY lname", 
 "dsn=pubs;uid=sa;pwd=;", 
 adOpenStatic, adLockOptimistic, adCmdText); 
 
 TESTHR(picRs->BindToRecordset(&rs)); 
 
 while (!pRs->EndOfFile) 
 { 
 // Process data in the CCustomRs C++ instance variables. 
 printf("Name = %s %s\n", 
 (rs.m_ul_fnameStatus == adFldOK ? rs.m_ch_fname: "<Error>"), 
 (rs.m_ul_lnameStatus == adFldOK ? rs.m_ch_lname: "<Error>")); 
 
 // Move to the next row of the Recordset. 
 // Fields in the new row will automatically be 
 // placed in the CCustomRs C++ instance variables. 
 
 pRs->MoveNext(); 
 } 
 } 
 catch (_com_error &e ) 
 { 
 printf("Error:\n"); 
 printf("Code = %08lx\n", e.Error()); 
 printf("Meaning = %s\n", e.ErrorMessage()); 
 printf("Source = %s\n", (LPCSTR) e.Source()); 
 printf("Description = %s\n", (LPCSTR) e.Description()); 
 } 
 ::CoUninitialize(); 
} 
```

