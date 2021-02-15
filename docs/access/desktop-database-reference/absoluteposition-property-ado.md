---
title: Свойство AbsolutePosition (ADO)
TOCTitle: AbsolutePosition property (ADO)
ms:assetid: 500be001-9fa1-177b-f19d-acf003a0cdc2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249259(v=office.15)
ms:contentKeyID: 48544787
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b5e25e014c6e93d35e3621bb9b5b3c21d5e77f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281979"
---
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="0d08b-102">Свойство AbsolutePosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="0d08b-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="0d08b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0d08b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0d08b-104">Указывает порядковую позицию текущей записи объекта [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0d08b-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="0d08b-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="0d08b-105">Settings and return values</span></span>

<span data-ttu-id="0d08b-106">Задает или возвращает  длинное значение от 1 до числа записей в объекте **Recordset** [(RecordCount)](recordcount-property-ado.md)или возвращает одно из [значений PositionEnum.](positionenum.md)</span><span class="sxs-lookup"><span data-stu-id="0d08b-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d08b-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="0d08b-107">Remarks</span></span>

<span data-ttu-id="0d08b-108">Чтобы установить **свойство AbsolutePosition,** ADO требует, чтобы поставщик OLE DB, который вы используете, реализовал интерфейс IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="0d08b-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="0d08b-109">При доступе к свойству **AbsolutePosition** объекта **Recordset,** открытого с помощью однонастроенного или динамического курсора, вызывается ошибка **adErrFeatureNotAvailable.**</span><span class="sxs-lookup"><span data-stu-id="0d08b-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span></span> <span data-ttu-id="0d08b-110">При других типах курсоров возвращается правильное положение, если поставщик поддерживает интерфейс IRowsetScroll.</span><span class="sxs-lookup"><span data-stu-id="0d08b-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span></span> <span data-ttu-id="0d08b-111">Если поставщик не поддерживает интерфейс *IRowsetScroll,* свойству задается свойство **adPosUnknown.**</span><span class="sxs-lookup"><span data-stu-id="0d08b-111">If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**.</span></span> <span data-ttu-id="0d08b-112">Чтобы определить, поддерживает ли он *IRowsetScroll, см. документацию по поставщику.*</span><span class="sxs-lookup"><span data-stu-id="0d08b-112">See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="0d08b-113">Используйте свойство **AbsolutePosition** для перемещения в запись на основе его порядкового положения в объекте **Recordset** или для определения порядкового положения текущей записи.</span><span class="sxs-lookup"><span data-stu-id="0d08b-113">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record.</span></span> <span data-ttu-id="0d08b-114">Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.</span><span class="sxs-lookup"><span data-stu-id="0d08b-114">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="0d08b-115">Как и [свойство AbsolutePage,](absolutepage-property-ado.md) **AbsolutePosition** основан на 1 и равен 1, когда текущая запись является первой записью в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="0d08b-115">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="0d08b-116">Общее число записей в объекте **Recordset** можно получить из свойства [RecordCount.](recordcount-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0d08b-116">You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="0d08b-117">При указании свойства **AbsolutePosition,** даже если оно является записью в текущем кэше, ADO перезагружает кэш новой группой записей, начиная с указанной вами записи.</span><span class="sxs-lookup"><span data-stu-id="0d08b-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="0d08b-118">Размер этой группы определяется свойством [CacheSize.](cachesize-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="0d08b-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="0d08b-119">Не следует использовать свойство **AbsolutePosition в качестве** заменяемого номера записи.</span><span class="sxs-lookup"><span data-stu-id="0d08b-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="0d08b-120">Положение заданной записи изменяется при удалении предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="0d08b-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="0d08b-121">Кроме того, нет гарантий, что для записи будет одинаковый **absolutePosition,** если объект **Recordset** повторно или повторно открыт.</span><span class="sxs-lookup"><span data-stu-id="0d08b-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="0d08b-122">Закладки по-прежнему являются рекомендуемой возможностью сохранения и возвращения в заданную позицию и являются единственным способом позиционирования во всех типах объектов **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="0d08b-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


