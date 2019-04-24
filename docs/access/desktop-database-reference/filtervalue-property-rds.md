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

Указывает значение, с которым отфильтровать записи.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. FilterValue = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*String* |**Строковое** значение, представляющее значение данных, с которым отфильтруются записи (например, "программист" или "125").|

## <a name="remarks"></a>Замечания

Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **FilterValue**, [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента. 

Функция сортировки упорядочивает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) . Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** записей на обновляемый. ****

Значения NULL приводят к ошибке несоответствия типа.

