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

Указывает, используется ли порядок сортировки по возрастанию или убыванию.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. SortDirection = *значение*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*Значение* |**Логическое** значение, которое при установке равное **true**указывает направление сортировки — по возрастанию. **Значение false** указывает на убывающий порядок.|

## <a name="remarks"></a>Замечания

Свойства [sortColumn](sortcolumn-property-rds.md), **SortDirection**, [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента. Функция сортировки упорядочивает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) . Метод **Reset** выполнит условия и заменит текущий **набор** записей на обновляемый. ****

