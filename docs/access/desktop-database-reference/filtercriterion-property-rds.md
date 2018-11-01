---
title: Свойство FilterCriterion (RDS)
TOCTitle: FilterCriterion Property (RDS)
ms:assetid: 51e6cb64-a404-114e-8e1a-0744cceeec3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249267(v=office.15)
ms:contentKeyID: 48544834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b5567265aba8d4490837ab69572a553d4aa1c1e1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869766"
---
# <a name="filtercriterion-property-rds"></a>Свойство FilterCriterion (RDS)


**Применимо к**: Access 2013, Office 2013



Указывает оператор оценки, используемый в значение фильтра.

## <a name="syntax"></a>Синтаксис

*DataControl*. FilterCriterion = *строка*

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *Строка*

  - **Строковое** значение, указывающее, оператор оценки [Значение_фильтра](filtervalue-property-rds.md) в записи. Может быть одним из следующих значений: \<, \<=, \>, \>=, =, или \< \>.

## <a name="remarks"></a>Замечания

[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), **FilterCriterion**и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

"\!=» Недопустимый оператор для **FilterCriterion**; Используйте "\<\>«.

Если задать свойства фильтрации и сортировки, вызовите метод **Сброс** набор строк сначала фильтруется и затем сортировки. Для сортировки в порядке возрастания, пустые значения отображаются сверху; для Сортировка по убыванию значения null, в нижней (по возрастанию — это поведение по умолчанию).

