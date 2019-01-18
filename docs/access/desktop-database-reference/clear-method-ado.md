---
title: Метод Clear - ActiveX Data Objects (ADO)
TOCTitle: Clear method (ADO)
ms:assetid: 5d51f42c-147b-1fcf-d05b-123e5714ecb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249329(v=office.15)
ms:contentKeyID: 48545110
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b0d76480bdb5d5a3ab258e103a00707af303a4d3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716861"
---
# <a name="clear-method-ado"></a>Метод Clear (ADO)


**Применимо к**: Access 2013, Office 2013

Удаляет все объекты **ошибок** из семейства **Errors** .

## <a name="syntax"></a>Синтаксис

*Ошибки*. Очистить

## <a name="remarks"></a>Замечания

Используйте метод **Clear** на семейство [Errors](errors-collection-ado.md) для удаления всех существующих объектов [Error](error-object-ado.md) из коллекции. При возникновении ошибки ADO автоматически удаляет семейство **Errors** и заполняется **Ошибка** объекты, основанные на новой ошибки.

Некоторые свойства и методы возвращают предупреждения, которые отображаются в виде объектов **ошибок** в семействе **Errors** , но не приостановить выполнение программы. Прежде чем обращаться [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)или [CancelBatch](cancelbatch-method-ado.md) методы объекта [набора записей](recordset-object-ado.md) ; метод [Open](open-method-ado-connection.md) объекта [подключения](connection-object-ado.md) ; или задать свойство [фильтра](filter-property-ado.md) для объекта **набора записей** , вызовите метод **Clear** на семейство **Errors** . Таким образом, могут читать свойство [Count](count-property-ado.md) коллекции **ошибок** для проверки возвращенных предупреждения.

