---
title: Свойство SortColumn (RDS)
TOCTitle: SortColumn property (RDS)
ms:assetid: 0a5d157c-9261-960d-6f89-33d9c94b3940
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248835(v=office.15)
ms:contentKeyID: 48543151
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54e6df1f2a94bd59f1e4cf9f9c0be77d785a3048
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306890"
---
# <a name="sortcolumn-property-rds"></a>Свойство SortColumn (RDS)

**Область применения**: Access 2013, Office 2013

Указывает, по каков столбец сортировать записи.

## <a name="syntax"></a>Синтаксис

*DataControl*. SortColumn = *String*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляюная [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*Строка* |**Строковая** строка, представляюная имя или псевдоним столбца для сортировки записей.|

## <a name="remarks"></a>Заметки

Свойства **SortColumn,** [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации в клиентском кэше. Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей сохраняется в кэше. Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий набор **recordset** на updatable **Recordset.**

Чтобы отсортировать набор **записей,** необходимо сначала сохранить ожидающих изменений. Если вы используете **RDS. DataControl**, можно использовать метод [SubmitChanges.](submitchanges-method-rds.md) Например, если **RDS. DataControl называется** ADC1, ваш код будет ADC1. SubmitChanges . If you are using an ADO **Recordset,** you can use its [UpdateBatch](updatebatch-method-ado.md) method. Использование **UpdateBatch** — это рекомендуемый метод для объектов **Recordset,** созданных с помощью [метода CreateRecordset.](createrecordset-method-rds.md) Например, ваш код может быть myRS.UpdateBatch или . If you are using an ADO **Recordset,** you can use its [UpdateBatch](updatebatch-method-ado.md) method. Использование **UpdateBatch** — это рекомендуемый метод для объектов **Recordset,** созданных с помощью метода [CreateRecordset.](createrecordset-method-rds.md) Например, ваш код может быть myRS.UpdateBatch или ADC1. Recordset.UpdateBatch .

