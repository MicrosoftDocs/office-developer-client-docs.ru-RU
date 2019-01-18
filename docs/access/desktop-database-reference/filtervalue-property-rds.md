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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721950"
---
# <a name="filtervalue-property-rds"></a>Свойство FilterValue (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает значение для фильтрации записей.

## <a name="syntax"></a>Синтаксис

*DataControl*. Значение_фильтра = *строка*

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|
|*String* |**Строковое** значение, представляющее значение данных для фильтрации записей (например, «Программиста» или 125).|

## <a name="remarks"></a>Замечания

[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), **Значение_фильтра**, [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. 

Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

Ошибка type mismatch привести значения NULL.

