---
title: Свойство Parameter.Value (DAO)
TOCTitle: Value Property
ms:assetid: 7058f3cd-9102-c711-bc83-b1565a8b001c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195733(v=office.15)
ms:contentKeyID: 48545556
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d4e7f3976b934c407a038f321953259fd63a6f60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287994"
---
# <a name="parametervalue-property-dao"></a>Свойство Parameter.Value (DAO)

**Область применения**: Access 2013, Office 2013

Задает или возвращает значение объекта. Для чтения и записи, **Variant**.

## <a name="syntax"></a>Синтаксис

*выражения* . Значение

*выражение* Переменная, представляюная **объект Параметр.**

## <a name="remarks"></a>Примечания

Значение параметра или значения возврата — это тип данных Variant, который оценивается до значения, соответствующего типу данных, указанному **свойством Type** объекта.

Как правило, **свойство Value** используется для получения и изменения данных в **объектах Recordset.**

Свойство **Value** — это свойство по умолчанию объектов **Field,** **Parameter** и **Property.** Таким образом, вы можете задать или вернуть значение одного из этих объектов, ссылаясь на них непосредственно, а не указать свойство **Value.**

Попытка установить или вернуть свойство **Value** в неподходящем контексте (например, свойство Value объекта **Field** в коллекции **Полей** объекта **TableDef)** приведет к ошибке, которая может быть заблокирована. 

> [!NOTE]
> При чтении десятичных значений из Microsoft SQL Server базы данных они будут отформатированы с помощью научной нотации через рабочее пространство Microsoft Access, но будут отображаться в качестве обычных десятичных значений через рабочее пространство ODBCDirect.


