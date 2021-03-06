---
title: Метод OpenSchema (ADO)
TOCTitle: OpenSchema method (ADO)
ms:assetid: 57771163-a14e-207a-2942-849acb79a9a1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249294(v=office.15)
ms:contentKeyID: 48544970
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 43ca69b9d761629d42138780517f8de806ed7e8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288338"
---
# <a name="openschema-method-ado"></a>Метод OpenSchema (ADO)

**Область применения**: Access 2013, Office 2013

Получает сведения о схеме базы данных от поставщика.

## <a name="syntax"></a>Синтаксис

**Набор***записей*  =  *подключение*. OpenSchema*(QueryType*, *Criteria*, *SchemaID*)

## <a name="return-values"></a>Возвращаемые значения

Возвращает объект [Recordset,](recordset-object-ado.md) содержащий сведения о схеме. **Recordset** будет открыт в качестве статического курсора только для чтения. *QueryType* определяет, какие столбцы отображаются в **Наборе записей.**

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*QueryType* |Любое [значение SchemaEnum,](schemaenum.md) которое представляет тип запроса схемы для выполнения.|
|*Criteria* |Необязательный параметр. Массив ограничений запросов для каждого *параметра QueryType,* как указано в **SchemaEnum.**|
|*SchemaID* |GUID для запроса схемы поставщика, не определенного спецификацией OLE DB. Этот параметр необходим, если *в QueryType* задан **параметр adSchemaProviderSpecific;** в противном случае он не используется.|

## <a name="remarks"></a>Примечания

Метод **OpenSchema** возвращает самоописательные сведения об источнике данных, например о таблицах в источнике данных, столбцах в таблицах и поддерживаемых типах данных.

Аргумент *QueryType* — это GUID, который указывает возвращенные столбцы (схемы). Спецификация OLE DB имеет полный список схем.

Аргумент *Criteria* ограничивает результаты запроса схемы. *Критерии* заданы массив значений, которые должны возникать в соответствующем подмножеству столбцов, называемых столбцами ограничений, в итоговом **Наборе записей.**

**Константа adSchemaProviderSpecific** используется для аргумента *QueryType,* если поставщик определяет собственные нестандартные запросы схемы за пределами перечисленных выше. При этом используется аргумент *SchemaID* для выполнения GUID запроса схемы. Если *в QueryType* задана **adSchemaProviderSpecific,** но *схемаid* не представлена, будет допущена ошибка.

Поставщики не обязаны поддерживать все стандартные запросы схемы OLE DB. В частности, спецификация OLE DB требует только **adSchemaTables,** **adSchemaColumns** и **adSchemaProviderTypes.** Однако поставщик не обязан поддерживать указанные выше ограничения *по* критериям для этих запросов схемы.

**Удаленное использование службы данных** Метод **OpenSchema** не доступен для объекта клиентского [подключения.](connection-object-ado.md)

> [!NOTE]
> В Visual Basic, столбцы с неподписаным набором четырехбайт (DBTYPE UI4) в наборе **Записей,** возвращаемого из метода **OpenSchema** на **объекте Подключение,** не могут сравниться с другими переменными. Дополнительные сведения о типах данных OLE DB см. в главе 13 и приложении A справочника программиста *Microsoft OLE DB.*


