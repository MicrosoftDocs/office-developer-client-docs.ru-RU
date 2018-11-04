---
title: Свойство FilterCriterion (RDS)
TOCTitle: FilterCriterion property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9887551d4d8a141c8390764bcd23c98c59edc26
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950225"
---
# <a name="filtercriterion-property-rds"></a>Свойство FilterCriterion (RDS)

**Применимо к**: Access 2013, Office 2013

Указывает оператор оценки, используемый в значение фильтра.

## <a name="syntax"></a>Синтаксис

*DataControl*. FilterCriterion = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.|
|*Строка* |**Строковое** значение, указывающее, оператор оценки [Значение_фильтра](filtervalue-property-rds.md) в записи. Может быть одним из следующих значений: \<, \<=, \>, \>=, =, или \< \>.|

## <a name="remarks"></a>Примечания

[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), **FilterCriterion**и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

"\!=» Недопустимый оператор для **FilterCriterion**; Используйте "\<\>«.

Если задать свойства фильтрации и сортировки, вызовите метод **Сброс** набор строк сначала фильтруется и затем сортировки. Для сортировки в порядке возрастания, пустые значения отображаются сверху; для Сортировка по убыванию значения null, в нижней (по возрастанию — это поведение по умолчанию).

