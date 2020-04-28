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

Интерфейс **ADORecordsetConstruction** используется для создания объекта ADO **Recordset** из объекта **набора строк** OLE DB в приложении C/C++.

Этот интерфейс поддерживает следующие свойства:

## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Части</a></p></td>
<td><p>Для чтения и записи.<br />
Получает или задает объект <strong>главы</strong> OLE DB от или on этого объекта <strong>Recordset</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Для чтения и записи.<br />
Получает/устанавливает объект <strong>ROWPOSITION</strong> OLE DB from/On этого объекта <strong>Recordset</strong> ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Возвращаем</a></p></td>
<td><p>Для чтения и записи.<br />
Получает или задает объект <strong>набора строк</strong> OLE DB from/On этого объекта <strong>Recordset</strong> ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methods

Нет.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Примечания

При наличии объекта **набора строк** OLE DB (провсет) построение объекта ADO **Recordset** (), **Создание объекта Recordset ADO (** адорс), будет иметь следующие три основные операции:

1. Создайте объект ADO **Recordset** :
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Запросите интерфейс **иадорекордсетконструктион** для объекта **Recordset** :

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Вызовите метод Иадорекордсетконструктион::p\_UT Rowset, чтобы задать объект набора строк OLE DB для объекта RECORDSET объекта ADO:

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
Объект Result теперь представляет объект **RECORDSET** ADO, созданный на основе объекта **набора строк** OLE DB.

Вы также можете создать объект ADO **Recordset** из **главы** OLE DB или объекта **RowPosition** .

## <a name="requirements"></a>Requirements

- **Версия:** ADO 2,0 и более поздние версии

- **Библиотека:** Msado15. dll

- **UUID:** 00000283-0000-0010-8000-00AA006D2EA4

