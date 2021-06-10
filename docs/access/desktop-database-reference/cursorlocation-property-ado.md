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

Указывает расположение службы курсоров.

## <a name="settings-and-return-values"></a>Параметры И значения возврата

Задает или возвращает **длинное** значение, которое можно установить к одному из [значений CursorLocationEnum.](cursorlocationenum.md)

## <a name="remarks"></a>Примечания

Это свойство позволяет выбирать между различными библиотеками курсоров, доступными поставщику. Обычно можно выбрать между использованием клиентской библиотеки курсоров или библиотекой, расположенной на сервере.

Этот параметр свойства влияет на подключения, установленные только после установки свойства. Изменение свойства **CursorLocation** не влияет на существующие подключения.

Курсоры, возвращенные методом [Execute,](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) наследуют этот параметр. **Объекты recordset** автоматически наследуют этот параметр из связанных подключений.

Это свойство является чтением или записью в [подключении](connection-object-ado.md) или закрытом наборе записей [и](recordset-object-ado.md)только для чтения в открытом **наборе записей.**

**Удаленное использование службы данных** Если используется в клиентском объекте **Recordset** или **Connection,** свойство **CursorLocation** можно задать только **adUseClient.**

