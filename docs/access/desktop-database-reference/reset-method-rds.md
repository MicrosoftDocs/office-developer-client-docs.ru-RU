---
title: Метод Reset (Справочник по базам данных для рабочих столов службы RDS)
TOCTitle: Reset method (RDS)
ms:assetid: 169ebd1e-6071-613e-c065-3af060167456
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248924(v=office.15)
ms:contentKeyID: 48543435
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 898045bcfdd3fb2483954155319e6aab3d0ebc7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306645"
---
# <a name="reset-method-rds"></a>Метод Reset (RDS)

**Область применения**: Access 2013, Office 2013

Выполняет сортировку или фильтрацию на клиентском объекте **Recordset** на основе указанных свойств сортировки и фильтра.

## <a name="syntax"></a>Синтаксис

*Элемент управления*. Сброс (*значение*)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*DataControl* |Объектная переменная, представляющая [RDS. Объект управления](datacontrol-object-rds.md) DataObject.|
|*value* |Необязательный атрибут. **Логическое** значение **true** (по умолчанию), если требуется фильтровать по текущему набору строк "filtered". **Значение false** означает, что выполняется фильтрация по исходному набору строк с удалением всех предыдущих параметров фильтра.|

## <a name="remarks"></a>Замечания

Свойства [sortColumn](sortcolumn-property-rds.md), [SortDirection](sortdirection-property-rds.md), [FilterValue](filtervalue-property-rds.md), [FilterCriterion](filtercriterion-property-rds.md)и [FilterColumn](filtercolumn-property-rds.md) предоставляют функции сортировки и фильтрации кэша на стороне клиента. Функция сортировки упорядочивает записи по значениям из одного столбца. Функция фильтрации отображает подмножество записей на основе условий поиска, а полный [набор записей](recordset-object-ado.md) сохраняется в кэше. Метод **Reset** выполнит условия и заменит текущий **набор** записей на обновляемый. ****

При изменении исходных данных, которые еще не были отправлены, метод **Reset** завершится с ошибками. Сначала используйте метод [SubmitChanges](submitchanges-method-rds.md) для сохранения изменений в **наборе записей**для чтения и записи, а затем используйте метод **Reset** для сортировки или фильтрации записей.

Если вы хотите выполнить несколько фильтров для набора строк, вы можете использовать необязательный *логический* аргумент с методом **Reset** . В приведенном ниже примере показано, как это сделать.

