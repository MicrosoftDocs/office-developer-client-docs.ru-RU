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

*Элемент управления*. FilterCriterion = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*String* |**Строковое** значение, задающее оператор оценки [FilterValue](filtervalue-property-rds.md) для записей. Может \<быть одним из следующих:, \<=, \>, \>=, = или. \< \>|

## <a name="remarks"></a>Замечания

Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), **FilterCriterion**и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента. Функция сортировки упорядочивает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) . Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** записей на обновляемый. ****

Недопустимый оператор "\!=" для **FilterCriterion**; Вместо этого используйте "\<\>".

Если заданы свойства Filter и Sort и вызван метод **Reset** , сначала выполняется фильтрация набора строк, а затем он сортируется. Для сортировки по возрастанию значения NULL отображаются сверху; для сортировки по убыванию значения NULL находятся в нижней части (по возрастанию это поведение по умолчанию).

