---
title: Supports method (ADO)
TOCTitle: Supports method (ADO)
ms:assetid: 2b4062ce-44df-4e84-1ce9-d6618c10c2af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249059(v=office.15)
ms:contentKeyID: 48543924
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 42447614c5fc58bc4eb2933354908693adf68ce6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308465"
---
# <a name="supports-method-ado"></a>Supports method (ADO)

**Область применения**: Access 2013, Office 2013

Определяет, поддерживает ли указанный [объект Recordset](recordset-object-ado.md) определенный тип функций.

## <a name="syntax"></a>Синтаксис

*boolean*  =  *recordset*. Supports *(CursorOptions)*

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **boolean,** которое указывает, поддерживаются ли поставщиком все функции, указанные аргументом *CursorOptions.*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*CursorOptions* |**Длинное** выражение, состоящее из одного или нескольких значений [CursorOptionEnum.](cursoroptionenum.md)|

## <a name="remarks"></a>Заметки

Используйте метод **Supports,** чтобы определить, какие типы функций поддерживает объект **Recordset.** Если объект **Recordset поддерживает** функции, соответствующие константы которых находятся в *cursorOptions,* метод **Supports** возвращает **true**. В противном случае возвращается **false.**


> [!NOTE]
> Хотя метод **Supports** может возвращать **true** для заданной функции, он не гарантирует, что поставщик сможет сделать эту функцию доступной при любых обстоятельствах. Метод **Supports** просто возвращает, может ли поставщик поддерживать указанные функции при условии, что выполнены определенные условия. Например, метод **Supports** может указывать на то, что объект **Recordset** поддерживает обновления, даже если курсор основан на нескольких скомплексе таблиц, некоторые столбцы которых не поддерживают обновление.


