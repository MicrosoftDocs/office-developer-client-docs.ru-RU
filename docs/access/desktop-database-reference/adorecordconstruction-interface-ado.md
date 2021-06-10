---
title: Интерфейс ADORecordConstruction (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281628"
---
# <a name="adorecordconstruction-interface-ado"></a>Интерфейс ADORecordConstruction (ADO)


**Область применения**: Access 2013, Office 2013

Интерфейс **ADORecordConstruction** используется для построения объекта ADO **Record** из объекта OLE DB **Row** в приложении C/C++.

Этот интерфейс поддерживает следующие свойства:

## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>Только для записи.<br />
Задает контейнер объекта OLE DB <strong>Row</strong> на этом объекте ADO <strong>Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Для чтения и записи.<br />
Получает/задает объект OLE DB <strong>Row</strong> из/на этом объекте ADO <strong>Record.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Методы

Нет.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Примечания

С учетом объекта OLE DB **Row** (pRow) строительство объекта ADO **Record** (adoR) составляет следующие три основные операции: 

1.  Создание объекта **записи** ADO:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Запрос **интерфейса IADORecordConstruction** на **объекте Запись:**
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Вызывай метод **свойства IADORecordConstruction::p ut \_ Row,** чтобы установить объект OLE DB **Row** на объекте ADO **Record:**
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
В результате объект **adoR представляет** объект ADO **Record,** построенный из объекта OLE DB **Row.**

Объект ADO **Record** также можно построить из контейнера объекта OLE DB **Row.**

## <a name="requirements"></a>Требования

**Версия:** ADO 2.0 и более поздний

**Библиотека:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

