---
title: Свойство field2. Value (DAO)
TOCTitle: Value Property
ms:assetid: 6ead6ba8-1613-99c7-7968-56f5b81b2385
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195566(v=office.15)
ms:contentKeyID: 48545515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4324917fcabd768a9527b11fceadbfc2dc9ef2b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292631"
---
# <a name="field2value-property-dao"></a>Свойство field2. Value (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта. Для чтения и записи, **Variant**.

## <a name="syntax"></a>Синтаксис

*Expression* . Оно

*expression* — переменная, представляющая объект **Field2**.

## <a name="remarks"></a>Примечания

Параметр или возвращаемое значение — это тип данных Variant, который оценивается как значение, соответствующее типу данных, как указано в свойстве **Type** объекта.

Как правило, свойство **value** используется для извлечения и изменения данных в объектах **Recordset** .

Свойство **value** является свойством по умолчанию для объектов **field2**, **Parameter**и **Property** . Таким образом, вы можете задать или вернуть значение одного из этих объектов, обратившись к ним напрямую вместо того, чтобы указывать свойство **value** .

Попытка задать или вернуть свойство **value** в неприемлемом контексте (например, свойство **value** объекта **field2** в коллекции **Fields** объекта **tabledef** ) приведет к ошибке перехвата.


> [!NOTE]
> При чтении десятичных значений из базы данных Microsoft SQL Server они будут отформатированы с использованием экспоненциальной нотации в рабочей области Microsoft Access, но будут отображаться как обычные десятичные значения в рабочей области ODBCDirect.


