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

Интерфейс **ADORecordConstruction** используется для создания объекта **записи** ADO из объекта **строки** OLE DB в приложении C/C++.

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
Задает контейнер объекта <strong>строки</strong> OLE DB для этого объекта <strong>записи</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Для чтения и записи.<br />
Получает или задает объект <strong>строки</strong> OLE DB от или on этого объекта <strong>записи</strong> ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Методы

Нет.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Замечания

ПоЛучив объект **строки** OLE DB (пров), создание объекта **записи** ADO (), создание объекта **записи** ADO (Адор), суммы для следующих трех базовых операций:

1.  Создание объекта **записи** ADO:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  ЗаПросите интерфейс **иадорекордконструктион** для объекта **Record** :
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  ВыЗовите метод **иадорекордконструктион::p\_UT Row** , чтобы задать объект **строки** OLE DB для объекта **записи** ADO:
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
Объект resultd **Адор** теперь представляет объект **записи** ADO, созданный на основе объекта **строки** OLE DB.

Объект **записи** ADO также может быть создан из контейнера объекта **строки** OLE DB.

## <a name="requirements"></a>Требования

**Версия:** ADO 2,0 и более поздние версии

**Библиотека:** Msado15. dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

