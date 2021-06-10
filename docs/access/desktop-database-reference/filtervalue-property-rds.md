---
title: Свойство FilterValue (RDS)
TOCTitle: FilterValue property (RDS)
ms:assetid: 66dc14cd-cc14-78cb-cb05-91eefb17ea47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249399(v=office.15)
ms:contentKeyID: 48545350
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70dca16f4a949cc6088779c1406e0c77cb477ba1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292407"
---
# <a name="filtervalue-property-rds"></a>Свойство FilterValue (RDS)

**Область применения**: Access 2013, Office 2013

Указывает значение для фильтрации записей.

## <a name="syntax"></a>Синтаксис

*DataControl*. FilterValue = *String*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*String* |Значение **String,** представляю которое представляет значение данных для фильтрации записей (например, "Программист" или 125).|

## <a name="remarks"></a>Примечания

Свойства [SortColumn,](sortcolumn-property-rds.md) [SortDirection,](sortdirection-property-rds.md) **FilterValue,** [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше. 

Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше. Метод [Reset](reset-method-rds.md) выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**

Значения Null приводит к ошибке несоответствия типа.

