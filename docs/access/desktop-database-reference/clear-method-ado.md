---
title: Метод Clear — ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0d76480bdb5d5a3ab258e103a00707af303a4d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296362"
---
# <a name="clear-method-ado"></a>Метод Clear (ADO)


**Область применения**: Access 2013, Office 2013

Удаляет все объекты **Error** из коллекции **Errors.**

## <a name="syntax"></a>Синтаксис

*Ошибки.* Очистить

## <a name="remarks"></a>Заметки

Используйте метод **Clear** для коллекции [Errors,](errors-collection-ado.md) чтобы удалить все существующие объекты [Error](error-object-ado.md) из коллекции. При ошибке ADO автоматически очищает коллекцию **Errors** и заполняет ее объектами **Error** в зависимости от новой ошибки.

Некоторые свойства и методы возвращают предупреждения, которые отображаются как объекты **Error** в коллекции **Errors,** но не останавливают выполнение программы. Перед вызовом [методов Resync,](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) для объекта [Recordset;](recordset-object-ado.md) Метод [Open](open-method-ado-connection.md) для объекта [Connection;](connection-object-ado.md) или установите свойство [Filter](filter-property-ado.md) для объекта **Recordset,** вызовите метод **Clear** в коллекции **Errors.** Таким образом можно считать свойство [Count](count-property-ado.md) коллекции **Errors** для проверки на возвращенных предупреждений.

