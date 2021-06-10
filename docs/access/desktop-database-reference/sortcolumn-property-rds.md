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

Указывает, в какой столбце сортировать записи.

## <a name="syntax"></a>Синтаксис

*DataControl*. SortColumn = *String*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Переменная объекта, представляюая [RDS. Объект DataControl.](datacontrol-object-rds.md)|
|*String* |**Строковая** величина, которая представляет имя или псевдоним столбца для сортировки записей.|

## <a name="remarks"></a>Примечания

Свойства **SortColumn,** [SortDirection,](sortdirection-property-rds.md) [FilterValue,](filtervalue-property-rds.md) [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) обеспечивают функции сортировки и фильтрации в клиентском кэше. Функция сортировки заказывает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе [](recordset-object-ado.md) критериев поиска, а полный набор записей поддерживается в кэше. Метод [Reset](reset-method-rds.md) выполнит критерии и заменит текущий **набор записей** на updatable **Recordset.**

Чтобы сортировать в **наборе Recordset,** сначала необходимо сохранить все ожидающих изменений. Если вы используете **RDS. DataControl**, вы можете использовать [метод SubmitChanges.](submitchanges-method-rds.md) Например, если ваш **RDS. DataControl** называется ADC1, код будет ADC1. SubmitChanges . Если вы используете ADO **Recordset,** вы можете использовать его [метод UpdateBatch.](updatebatch-method-ado.md) Использование **UpdateBatch** — это рекомендуемый метод для объектов **Recordset,** созданных с помощью [метода CreateRecordset.](createrecordset-method-rds.md) Например, код может быть myRS.UpdateBatch или . Если вы используете ADO **Recordset,** вы можете использовать его [метод UpdateBatch.](updatebatch-method-ado.md) Использование **UpdateBatch** — это рекомендуемый метод для объектов **Recordset,** созданных с помощью [метода CreateRecordset.](createrecordset-method-rds.md) Например, код может быть myRS.UpdateBatch или ADC1. Recordset.UpdateBatch .

