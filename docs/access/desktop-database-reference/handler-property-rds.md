---
title: Свойство Handler (RDS)
TOCTitle: Handler property (RDS)
ms:assetid: aaf8c8c6-f95b-3cf3-b3f6-203f37464c87
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249792(v=office.15)
ms:contentKeyID: 48546962
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c3ad91f0a288b9908a5af5f92d7bfca3b23cdfe9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292071"
---
# <a name="handler-property-rds"></a>Свойство Handler (RDS)

**Область применения**: Access 2013, Office 2013

Указывает имя программы настройки на стороне сервера (обработчика), которая расширяет функциональные возможности [RDSServer.DataFactory](datafactory-object-rdsserver.md)и любые параметры, используемые обработчиком. 

## <a name="syntax"></a>Синтаксис

*DataControl*. Handler = *String*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*Строка* |**Строковое** значение, которое содержит имя обработвода и все параметры, разделенные запятой (например, "handlerName,parm1,parm2,...,parm *N"*).|

## <a name="remarks"></a>Заметки

Это свойство поддерживает настройку, функциональность, требуемую установки свойству [CursorLocation](cursorlocation-property-ado.md) свойства **adUseClient.**

Имя обработера и его параметры(если таковые имеются) разделяются запятой (","). Непредсказуемое поведение приведет, если в строке появится точку с за точкой с зачетом *(";").* Можно написать собственный обработчик, если он поддерживает интерфейс **IDataFactoryHandler.**

Имя обработера по умолчанию **— MSDFMAP. Обработок** и его параметр по умолчанию — это файл настройки **с именемMSDFMAP.INI.** Это свойство используется для вызова альтернативных файлов настройки, созданных администратором сервера.

В качестве альтернативы настройке **свойства Handler** можно указать обработок и параметры в [свойстве ConnectionString;](connectionstring-property-ado.md) то есть"**Handler=***handlerName,parm1,parm2,...;*".

