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

Интерфейс **ADORecordConstruction** используется для создания объекта записи **ADO** из объекта строки OLE **DB** в приложении C/C++.

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
Задает контейнер объекта строки OLE <strong>DB</strong> для этого объекта <strong>записи</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Для чтения и записи.<br />
Получает или задает объект строки OLE <strong>DB</strong> из/на этом объекте <strong>записи</strong> ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Methods

Нет.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Заметки

С учетом объекта строки OLE **DB** (pRow) при конструкции объекта записи **ADO** (adoR) конструкция объекта записи ADO (adoR) составляет следующие три основные операции: 

1.  Создание объекта **записи** ADO:
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Запрос **интерфейса IADORecordConstruction** объекта **Record:**
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Вызовите метод свойства **IADORecordConstruction::p ut \_ Row,** чтобы установить объект строки OLE **DB** в объекте ADO **Record:**
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
После этого **объект adoR** представляет объект записи **ADO,** построенный из объекта строки OLE **DB.**

Объект **записи** ADO также можно построить из контейнера объекта строки OLE **DB.**

## <a name="requirements"></a>Требования

**Версия:** ADO 2.0 и более поздние

**Библиотека:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

