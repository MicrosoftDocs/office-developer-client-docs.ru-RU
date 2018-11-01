---
title: Свойство AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: a090630b5db741f761314f598fcc783dd124d1cf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881862"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="268ce-102">Свойство AbsolutePosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="268ce-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="268ce-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="268ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="268ce-104">Указывает порядковый номер текущей записи объекта [набора записей](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="268ce-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="268ce-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="268ce-105">Settings and return values</span></span>

<span data-ttu-id="268ce-106">Задает или возвращает значение типа **Long** от 1 число записей в объекте **набора записей** ([RecordCount](recordcount-property-ado.md)) либо одно из значений [PositionEnum](positionenum.md) .</span><span class="sxs-lookup"><span data-stu-id="268ce-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="268ce-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="268ce-107">Remarks</span></span>

<span data-ttu-id="268ce-108">Чтобы задать свойство **AbsolutePosition** , ADO требует, что поставщика OLE DB, который вы используете реализовать интерфейс IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="268ce-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="268ce-109">Доступ к **AbsolutePosition** свойство **набора записей** , который был открыт для последовательного доступа или динамический курсор вызывает ошибки **adErrFeatureNotAvailable**.</span><span class="sxs-lookup"><span data-stu-id="268ce-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span></span> <span data-ttu-id="268ce-110">Другие типы курсора надлежащих позициях будут возвращены до тех пор, пока поставщик поддерживает интерфейс IRowsetScroll.</span><span class="sxs-lookup"><span data-stu-id="268ce-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span></span> <span data-ttu-id="268ce-111">Если поставщик поддерживает интерфейс *IRowsetScroll* , свойство имеет значение **adPosUnknown**.</span><span class="sxs-lookup"><span data-stu-id="268ce-111">If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**.</span></span> <span data-ttu-id="268ce-112">Обратитесь к документации для поставщика, чтобы определить, поддерживает ли *IRowsetScroll*.</span><span class="sxs-lookup"><span data-stu-id="268ce-112">See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="268ce-113">Используйте свойство **AbsolutePosition** для переноса записей по его порядковый номер в объекте **набора записей** или для определения порядковый номер текущей записи.</span><span class="sxs-lookup"><span data-stu-id="268ce-113">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record.</span></span> <span data-ttu-id="268ce-114">Поставщик должен поддерживать соответствующие функциональные возможности для этого свойства, чтобы оно было доступно.</span><span class="sxs-lookup"><span data-stu-id="268ce-114">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="268ce-115">Как и свойство [AbsolutePage](absolutepage-property-ado.md) **AbsolutePosition** на основе 1 и имеет значение 1, если текущая запись является первой записи в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="268ce-115">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="268ce-116">Общее число записей в объекте **набора записей** можно получить из свойства [RecordCount](recordcount-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="268ce-116">You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="268ce-117">Если задать свойство **AbsolutePosition** даже в том случае, если это записи в текущей кэш-памяти, ADO перезагружает кэша с новой группы записей, начиная с записью, указанной.</span><span class="sxs-lookup"><span data-stu-id="268ce-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="268ce-118">Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.</span><span class="sxs-lookup"><span data-stu-id="268ce-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="268ce-119">Не следует использовать свойство **AbsolutePosition** как номер заменяющего записи.</span><span class="sxs-lookup"><span data-stu-id="268ce-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="268ce-120">Положение данной записи изменений при удалении предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="268ce-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="268ce-121">Нет никакой гарантии, что данной записи будут иметь же **AbsolutePosition** , если опросить или повторном открытии в объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="268ce-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="268ce-122">Закладки по-прежнему не рекомендуемый способ сохранения и возврата в заданной позиции, а также являются единственным способом размещения для всех типов объектов **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="268ce-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


