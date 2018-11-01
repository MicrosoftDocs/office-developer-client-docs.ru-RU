---
title: Свойство SortColumn (RDS)
TOCTitle: SortColumn Property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a613ed053bd91685286066bfa534c41b99edbdd1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874757"
---
# <a name="sortcolumn-property-rds"></a>Свойство SortColumn (RDS)


**Применимо к**: Access 2013, Office 2013

Указывает, какой столбец для сортировки записей.

## <a name="syntax"></a>Синтаксис

*DataControl*. SortColumn = *строка*

## <a name="parameters"></a>Параметры

  - *DataControl*

  - Объектную переменную, которая представляет [RDS. DataControl](datacontrol-object-rds.md) объекта.

  - *Строка*

  - **Строковое** значение, представляющее имя или псевдоним столбца, по которому выполняется сортировка записей.

## <a name="remarks"></a>Замечания

**SortColumn**, [SortDirection](sortdirection-property-rds.md), [Значение_фильтра](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) свойства предоставляют функциональные возможности сортировки и фильтрации на кэш со стороны клиента. Функциональные возможности сортировки упорядочивает записей по значениями, полученными из одного столбца. Функции фильтрации отображает подмножество записей на основании условия поиска, пока сохраняется полный [набор записей](recordset-object-ado.md) в кэше. Метод [Reset](reset-method-rds.md) будет выполнять критерии и замените текущего **набора записей** обновляемых **записей**.

Для сортировки по **записей**, необходимо предварительно сохранить все ожидающие изменения. Если вы используете **RDS. DataControl**, можно использовать метод [SubmitChanges](submitchanges-method-rds.md) . Например если ваше **RDS. DataControl** — с именем ADC1, код может быть ADC1. SubmitChanges. При использовании набора **записей**ADO можно использовать его метод [UpdateBatch](updatebatch-method-ado.md) . С помощью **UpdateBatch** рекомендуется для объектов **набора записей** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) . Например, код может быть myRS.UpdateBatch или. При использовании набора **записей**ADO можно использовать его метод [UpdateBatch](updatebatch-method-ado.md) . С помощью **UpdateBatch** рекомендуется для объектов **набора записей** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) . Например код может быть myRS.UpdateBatch или ADC1. Recordset.UpdateBatch.

