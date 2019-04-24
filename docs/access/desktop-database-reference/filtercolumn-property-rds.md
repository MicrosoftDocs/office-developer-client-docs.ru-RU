---
title: Свойство FilterColumn (RDS)
TOCTitle: FilterColumn property (RDS)
ms:assetid: fb5d9f23-b62a-8131-d6ff-8b7ed8bb825c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250287(v=office.15)
ms:contentKeyID: 48548868
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d29c591c88de4b53535c26430bf369cbd3f53284
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292442"
---
# <a name="filtercolumn-property-rds"></a>Свойство FilterColumn (RDS)

**Область применения**: Access 2013, Office 2013

Указывает столбец, для которого необходимо оценить условия фильтра.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. FilterColumn = *строка*

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*String* |**Строковое** значение, задающее столбец, для которого необходимо оценить условия фильтра. Условия фильтра указываются в свойстве [FilterCriterion](filtercriterion-property-rds.md) .|

## <a name="remarks"></a>Замечания

Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и **FilterColumn** предоставляют функции сортировки и фильтрации кэша на стороне клиента. 

Функция сортировки упорядочивает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе критериев поиска, в то время как в кэше сохраняется полный [набор записей](recordset-object-ado.md) . 

Метод [Reset](reset-method-rds.md) выполнит условия и заменит текущий **набор** записей на обновляемый. ****

