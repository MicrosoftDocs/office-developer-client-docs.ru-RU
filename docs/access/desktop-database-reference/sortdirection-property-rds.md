---
title: Свойство SortDirection (RDS)
TOCTitle: SortDirection property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fd09eb22d9f751ab1140db948356d2b168b30afb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308619"
---
# <a name="sortdirection-property-rds"></a>Свойство SortDirection (RDS)

**Область применения**: Access 2013, Office 2013

Указывает, является ли порядок сортировки по возрастанию или убыванию.

## <a name="syntax"></a>Синтаксис

*DataControl*. SortDirection = *value*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*Значение* |**Boolean** value that, when set to **True,** indicates the sort direction is ascending. **False** указывает на убывающий порядок.|

## <a name="remarks"></a>Заметки

Свойства [SortColumn,](sortcolumn-property-rds.md) **SortDirection,** [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают сортировку и фильтрацию в клиентском кэше. Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей сохраняется в кэше. Метод **Reset** выполнит условия и заменит текущий набор **recordset** на updatable **Recordset.**

