---
title: Свойство CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295222"
---
# <a name="cursorlocation-property-ado"></a>Свойство CursorLocation (ADO)


**Область применения**: Access 2013, Office 2013

Указывает расположение службы курсора.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Long** , которое может быть равно одному из значений [курсорлокатионенум](cursorlocationenum.md) .

## <a name="remarks"></a>Примечания

Это свойство позволяет выбирать между различными библиотеками курсоров, доступными для поставщика. Как правило, можно выбрать использование клиентской библиотеки курсоров или на сервере, расположенном на сервере.

Этот параметр свойства влияет на подключения, установленные только после задания свойства. Изменение свойства **CursorLocation** не оказывает никакого действия для существующих подключений.

Курсоры, возвращаемые методом [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) , наследуют этот параметр. Объекты **Recordset** будут автоматически наследовать этот параметр от связанных подключений.

Это свойство доступно для чтения и записи для [подключения](connection-object-ado.md) или закрытого [набора записей](recordset-object-ado.md)и доступно только для чтения в открытом **наборе записей**.

**Использование удаленной службы данных** При использовании в объекте **Recordset** или объекте **подключения** на стороне клиента для свойства **CursorLocation** можно задать только значение **адусеклиент**.

