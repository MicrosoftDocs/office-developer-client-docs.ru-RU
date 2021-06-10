---
title: Свойство FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 65541e8f64c5a019679252246edbe8027130c4ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292428"
---
# <a name="filtercriterion-property-rds"></a>Свойство FilterCriterion (RDS)

**Область применения**: Access 2013, Office 2013

Указывает оператор оценки для использования в значении фильтра.

## <a name="syntax"></a>Синтаксис

*DataControl*. FilterCriterion = *String*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*String* |Значение **String,** которое указывает оператор оценки [FilterValue](filtervalue-property-rds.md) для записей. Может быть любой из следующих: \< \< =, \> \> =, =, =, или \< \> .|

## <a name="remarks"></a>Примечания

Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) **FilterCriterion** и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше. Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше. Метод [Reset](reset-method-rds.md) выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**

Оператор \! "=" не действителен для **FilterCriterion;** вместо этого используйте \< \> ".

Если установлены свойства фильтра и сортировки, и вы называете метод **Reset,** сначала фильтруется набор строк, а затем сортироваться. Для восходящих сортов значения null находятся в верхней части; для убывающих сортов значения null находятся в нижней части (восходящий — это поведение по умолчанию).

