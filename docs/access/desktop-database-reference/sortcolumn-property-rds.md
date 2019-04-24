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

Указывает, по какому столбцу следует отсортировать записи.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. SortColumn = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*String* |**Строковое** значение, представляющее имя или псевдоним столбца, по которому сортируются записи.|

## <a name="remarks"></a>Замечания

Свойства **sortColumn**, [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента. Функция сортировки упорядочивает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) . Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** записей на обновляемый. ****

Для сортировки по **набору записей**сначала необходимо сохранить все ожидающие изменения. Если вы используете **RDS. Элемент управления**, вы можете использовать метод [SubmitChanges](submitchanges-method-rds.md) . Например, если вы **RDS. Элемент управления** ADC1 с именем, код будет ADC1. SubmitChanges. Если вы используете **набор записей**ADO, вы можете использовать его метод [UpdateBatch](updatebatch-method-ado.md) . Использование **UpdateBatch** является рекомендуемым методом для объектов **Recordset** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) . Например, ваш код может быть Мирс. UpdateBatch или. Если вы используете **набор записей**ADO, вы можете использовать его метод [UpdateBatch](updatebatch-method-ado.md) . Использование **UpdateBatch** является рекомендуемым методом для объектов **Recordset** , созданных с помощью метода [CreateRecordset](createrecordset-method-rds.md) . Например, ваш код может быть Мирс. UpdateBatch или ADC1. Recordset. UpdateBatch.

