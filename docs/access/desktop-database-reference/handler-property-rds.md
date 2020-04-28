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

Указывает имя программы настройки на стороне сервера (обработчика), расширяющей функциональные возможности [рдссервер.](datafactory-object-rdsserver.md), и все параметры, используемые *обработчиком*.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. Обработчик = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*String* |**Строковое** значение, содержащее имя обработчика и все параметры, разделенные запятыми (например, "хандлернаме, parm1, parm2,..., ПАРМ *N*").|

## <a name="remarks"></a>Примечания

Это свойство поддерживает настройку, которая требует установки свойства [CursorLocation](cursorlocation-property-ado.md) в **адусеклиент**.

Имя обработчика и его параметры разделяются запятыми (","). Непредсказуемое поведение приведет к появлению точки с запятой (";") в любом месте *строки*. Вы можете написать собственный обработчик, при условии, что он поддерживает интерфейс **идатафакторихандлер** .

Имя обработчика по умолчанию — **мсдфмап. , А**его параметр по умолчанию — файл настройки с именем **мсдфмап. INI**. Используйте это свойство, чтобы вызвать альтернативные файлы настройки, созданные администратором сервера.

Альтернативой заданию свойства **handler** является указание обработчика и параметров в свойстве [ConnectionString](connectionstring-property-ado.md) ; то есть "**handler = * * * хандлернаме, parm1, parm2,...;*".

