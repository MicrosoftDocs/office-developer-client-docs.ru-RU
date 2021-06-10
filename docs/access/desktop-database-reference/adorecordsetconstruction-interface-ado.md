---
title: Интерфейс ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281635"
---
# <a name="adorecordsetconstruction-interface-ado"></a>Интерфейс ADORecordsetConstruction (ADO)


**Область применения**: Access 2013, Office 2013

Интерфейс **ADORecordsetConstruction** используется для построения объекта ADO **Recordset** из объекта **Rowset** OLE DB в приложении C/C++.

Этот интерфейс поддерживает следующие свойства:

## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Глава</a></p></td>
<td><p>Для чтения и записи.<br />
Получает/задает объект главы OLE DB <strong>из/на</strong> этом объекте ADO <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Для чтения и записи.<br />
Получает/задает объект <strong>RowPosition</strong> OLE DB из/на этом объекте ADO <strong>Recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Для чтения и записи.<br />
Получает/задает объект OLE DB <strong>Rowset</strong> из/на этом объекте ADO <strong>Recordset.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Методы

Нет.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Примечания

С учетом объекта OLE DB **Rowset** (pRowset), при строительстве объекта ADO **Recordset** (), строительство объекта ADO **Recordset** (adoRs) составляет следующие три основные операции:

1. Создание объекта ADO **Recordset:**
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Запрос **интерфейса IADORecordsetConstruction** на **объекте Recordset:**

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Вызов свойства IADORecordsetConstruction::p ut Rowset, чтобы установить объект \_ OLE DB Rowset на объекте ADO Recordset:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
В результате объект представляет объект ADO **Recordset,** построенный из объекта **Rowset** OLE DB.

Можно также создать объект ADO **Recordset** из главы OLE **DB** или **объекта RowPosition.**

## <a name="requirements"></a>Требования

- **Версия:** ADO 2.0 и более поздний

- **Библиотека:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

