---
title: Свойство Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98aeb3a56203fd5adbeb5b58a1298a7b1df98439
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950134"
---
# <a name="handler-property-rds"></a>Свойство Handler (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает имя программы настройки на сервере (обработчик), которая расширяет возможности [RDSServer.DataFactory](datafactory-object-rdsserver.md)и все параметры, используемые в *обработчик*.

## <a name="syntax"></a>Синтаксис

*DataControl*. Обработчик = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|
|*Строка* |**Строковое** значение, содержащее имя обработчика и любых параметров, все запятыми (например, «handlerName, parm1, parm2,..., parm *N*»).|

## <a name="remarks"></a>Примечания

Это свойство поддерживает настройки, функциональные возможности, необходимо задать свойство [CursorLocation](cursorlocation-property-ado.md) **adUseClient**.

Имя обработчика и ее параметры при их наличии, разделенных запятыми («,»). Непредсказуемое поведение приведет к, если точку с запятой («;») в любом месте отображается в *строке*. Можно создать собственный обработчик условии, что он поддерживает интерфейс **IDataFactoryHandler** .

Имя обработчика по умолчанию — **MSDFMAP. Обработчик**, и его параметр по умолчанию — это файл настройки с именем **MSDFMAP. INI**. Это свойство используется для вызова настройки альтернативного файлы, созданные администратором сервера.

Альтернатива для установки свойства **обработчика** — указание обработчика и параметры в свойство [ConnectionString](connectionstring-property-ado.md) ; то есть «**обработчик = *** handlerName, parm1, parm2,...;*«.

