---
title: FilterColumn Property (RDS)
TOCTitle: FilterColumn Property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 459fc61dbb8c8b1eecffdea3d2c5d2f105b9212a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480619"
---
# <a name="filtercolumn-property-rds"></a>FilterColumn Property (RDS)


**Применимо к**: Access 2013 | Office 2013



Указывает столбец, по которому для оценки условия фильтра.

## <a name="syntax"></a>Синтаксис

*DataControl*. FilterColumn = *строка*

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *Строка*

  - **Строковое** значение, указывающее, столбец, по которому для оценки условия фильтра. Условия фильтра указанных в свойстве [FilterCriterion](filtercriterion-property-rds.md) .

## <a name="remarks"></a>Замечания

[SortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

