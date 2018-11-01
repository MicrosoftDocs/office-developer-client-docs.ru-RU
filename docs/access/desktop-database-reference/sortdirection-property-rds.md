---
title: Свойство направления сортировки (RDS)
TOCTitle: SortDirection Property (RDS)
ms:assetid: 33de0dce-f371-6a54-d179-0627939f5b14
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249106(v=office.15)
ms:contentKeyID: 48544119
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3603696992ab7ac759a62a70f50b4fa35636d2c0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879153"
---
# <a name="sortdirection-property-rds"></a>Свойство направления сортировки (RDS)


**Применимо к**: Access 2013, Office 2013


Указывает, будет ли порядок сортировки по возрастанию или по убыванию.

## <a name="syntax"></a>Синтаксис

*DataControl*. Направления сортировки = *значение*

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *Значение*

  - **Логическое** значение, если параметр имеет значение **True**, указывающее направление сортировки по возрастанию. **Значение false** указывает убывающем порядке.

## <a name="remarks"></a>Замечания

[SortColumn](sortcolumn-property-rds.md), **SortDirection**, [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод **Reset** будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

