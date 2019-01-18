---
title: Метод Refresh (ADO)
TOCTitle: Refresh method (ADO)
ms:assetid: f1c8829f-9c7d-12b6-7470-727ff38d663e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250227(v=office.15)
ms:contentKeyID: 48548631
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bd7c47e7c3e41a7b42571043cfafc9e4e909a9f9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710589"
---
# <a name="refresh-method-ado"></a>Метод Refresh (ADO)

**Применимо к**: Access 2013, Office 2013

Обновление объектов в коллекции объектов, доступных из и относящиеся к поставщику.

## <a name="syntax"></a>Синтаксис

*семейства сайтов*. Обновление

## <a name="remarks"></a>Замечания

Метод **Refresh** выполняет различные задачи в зависимости от семейства сайтов, из которого вызывается его.

## <a name="parameters"></a>Parameters

С помощью метода **обновления** на коллекцию [параметров](parameters-collection-ado.md) объекта [команда](command-object-ado.md) получает сведения о параметрах стороне поставщика для хранимой процедуры или параметризованный запрос, указанный в объекте **команды** . Коллекция будет пустым для поставщиков, которые не поддерживают вызовы хранимых процедур и запросов с заданными параметрами.

Должно значение свойства [ActiveConnection](activeconnection-property-ado.md) объекта **команды** на допустимый объект [подключения](connection-object-ado.md) , свойства [CommandText](commandtext-property-ado.md) допустимой команды и свойства [CommandType](commandtype-property-ado.md) **adCmdStoredProc** перед вызов метода **обновления** .

Если доступ к коллекции **параметров** до вызова метода **обновления на** ADO автоматически вызовите метод и заполнения в коллекции.

> [!NOTE]
> Если использовать метод **Refresh** для получения сведений о параметрах от поставщика, и он возвращает тип данных переменной длины один или несколько объектов [параметров](parameter-object-ado.md) , ADO может выделить память для параметров, основанных на их максимальный размер потенциальных, который будет возникает ошибка во время выполнения. Необходимо явно задать свойство [размер](size-property-ado.md) для этих параметров до вызова метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) для предотвращения ошибок.

### <a name="fields"></a>Поля

С помощью метода **обновления** на коллекции **полей** не действует видимым. Чтобы извлечь изменения из базовой структуры базы данных, необходимо использовать либо метод [повторный запрос](requery-method-ado.md) или, если объекта [набора записей](recordset-object-ado.md) не поддерживает закладки, метод [MoveFirst](movefirst-movelast-movenext-and-moveprevious-methods-ado.md) .

### <a name="properties"></a>Свойства

С помощью метода **обновления** на коллекцию **свойств** некоторые объекты заполняет коллекцию динамические свойства, предоставляемые поставщиком. Эти свойства предоставляют сведения о конкретных функциях к поставщику за пределы для поддержки ADO встроенных свойств.

