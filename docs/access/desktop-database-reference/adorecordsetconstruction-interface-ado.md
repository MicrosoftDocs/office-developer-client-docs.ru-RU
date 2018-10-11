---
title: ADORecordsetConstruction Interface (ADO)
TOCTitle: ADORecordsetConstruction Interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0b99fcfe4fadc3dddf5937ba1043875de43e88d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482081"
---
# <a name="adorecordsetconstruction-interface-ado"></a>ADORecordsetConstruction Interface (ADO)


**Применимо к**: Access 2013 | Office 2013

Интерфейс **ADORecordsetConstruction** используется для создания объекта ADO **записей** из объекта OLE DB **строк** в приложении C/C++.

Этот интерфейс поддерживает следующие свойства:

## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Главы</a></p></td>
<td><p>Чтение и запись.<br />
Получает или задает объект OLE DB <strong>главы</strong> из/на этот объект ADO <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Чтение и запись.<br />
Получает или задает объект OLE DB <strong>RowPosition</strong> из/на этот объект ADO <strong>Recordset</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Набор строк</a></p></td>
<td><p>Чтение и запись.<br />
Получает или задает объект OLE DB <strong>строк</strong> из/на этот объект ADO <strong>Recordset</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Методы

Отсутствуют.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Замечания

Получает объект OLE DB **строк** (pRowset), конструкции (объект ADO **набора записей** ), конструкции суммы (adoRs) объект ADO **набора записей** к три базовых операций:

1. Создайте объект ADO **набора записей** :
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Запрос интерфейс **IADORecordsetConstruction** объекта **набора записей** :

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Вызов IADORecordsetConstruction::put\_метод свойства строк установить объект строк OLE DB для объекта набора записей ADO:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
Результирующий объект теперь представляет объект ADO **записей** , созданный из объекта OLE DB **строк** .

Также можно создать объект ADO **записей** из объекта OLE DB **главы** или **RowPosition** .

## <a name="requirements"></a>Требования

- **Версия:** ADO 2.0 и более поздних версий

- **Библиотеки:** msado15.dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

