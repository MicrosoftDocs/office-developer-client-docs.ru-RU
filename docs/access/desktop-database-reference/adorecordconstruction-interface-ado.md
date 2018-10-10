---
title: ADORecordConstruction Interface (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44272067d8018836fd7eb3d6cfaa762780f69868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481482"
---
# <a name="adorecordconstruction-interface-ado"></a>ADORecordConstruction Interface (ADO)


**Применимо к**: Access 2013 | Office 2013

Интерфейс **ADORecordConstruction** используется для создания объекта ADO **записи** из объекта OLE DB **строки** в приложении C/C++.

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
Задает контейнер объекта OLE DB <strong>строку</strong> на этот объект ADO <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="row-property-ado.md">Строка</a></p></td>
<td><p>Чтение и запись.<br />
Получает или задает объект OLE DB <strong>строку</strong> из/на этот объект ADO <strong>записи</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Методы

Отсутствуют.

## <a name="events"></a>События

Нет.

## <a name="remarks"></a>Замечания

Заданным объекта OLE DB **строки** (pRow), конструкции (объект ADO **записи** ), конструирование объекта ADO **записи** (adoR) объемов для трех основных операций:

1.  Создайте объект ADO **записи** :
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  Запрос интерфейс **IADORecordConstruction** объекта **записи** :
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  Вызов **IADORecordConstruction::put\_строки** метод свойства, чтобы установить для объекта OLE DB **строку** на объект ADO **записи** :
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
Объект результирующее **adoR** теперь представляет объект ADO **записи** , созданный из объекта OLE DB **строки** .

Объект ADO **записи** также могут быть созданы из контейнера OLE DB **строки** объекта.

## <a name="requirements"></a>Требования

**Версия:** ADO 2.0 и более поздних версий

**Библиотеки:** msado15.dll

**UUID:** 00000567-0000-0010-8000-00AA006D2EA4

