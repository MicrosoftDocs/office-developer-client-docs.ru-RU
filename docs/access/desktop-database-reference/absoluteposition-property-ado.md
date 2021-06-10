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
# <a name="absoluteposition-property-ado"></a><span data-ttu-id="70904-102">Свойство AbsolutePosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="70904-102">AbsolutePosition property (ADO)</span></span>

<span data-ttu-id="70904-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70904-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70904-104">Указывает расположение текущей записи объекта [Recordset.](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="70904-104">Indicates the ordinal position of a [Recordset](recordset-object-ado.md) object's current record.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="70904-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="70904-105">Settings and return values</span></span>

<span data-ttu-id="70904-106">Задает или возвращает значение **Long** от 1 до количества записей в объекте **Recordset** [(RecordCount)](recordcount-property-ado.md)или возвращает одно из [значений PositionEnum.](positionenum.md)</span><span class="sxs-lookup"><span data-stu-id="70904-106">Sets or returns a **Long** value from 1 to the number of records in the **Recordset** object ([RecordCount](recordcount-property-ado.md)), or returns one of the [PositionEnum](positionenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="70904-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="70904-107">Remarks</span></span>

<span data-ttu-id="70904-108">Чтобы установить **свойство AbsolutePosition,** ADO требует, чтобы поставщик OLE DB, который вы используете, реализовал интерфейс IRowsetLocate.</span><span class="sxs-lookup"><span data-stu-id="70904-108">To set the **AbsolutePosition** property, ADO requires that the OLE DB provider you are using implement the IRowsetLocate interface.</span></span>

<span data-ttu-id="70904-109">Доступ к свойству **AbsolutePosition** для наборов **записей,** открываемых только вперед или динамическим курсором, вызывает ошибку **adErrFeatureNotAvailable.**</span><span class="sxs-lookup"><span data-stu-id="70904-109">Accessing the **AbsolutePosition** property of a **Recordset** that was opened with either a forward-only or dynamic cursor raises the error **adErrFeatureNotAvailable**.</span></span> <span data-ttu-id="70904-110">С другими типами курсоров правильная позиция возвращается до тех пор, пока поставщик поддерживает интерфейс IRowsetScroll.</span><span class="sxs-lookup"><span data-stu-id="70904-110">With other cursor types, the correct position will be returned as long as the provider supports the IRowsetScroll interface.</span></span> <span data-ttu-id="70904-111">Если поставщик не поддерживает *интерфейс IRowsetScroll,* свойство настроено **на adPosUnknown**.</span><span class="sxs-lookup"><span data-stu-id="70904-111">If the provider does not support the *IRowsetScroll* interface, the property is set to **adPosUnknown**.</span></span> <span data-ttu-id="70904-112">См. документацию для поставщика, чтобы определить, поддерживает ли он *IRowsetScroll.*</span><span class="sxs-lookup"><span data-stu-id="70904-112">See the documentation for your provider to determine whether it supports *IRowsetScroll*.</span></span>

<span data-ttu-id="70904-113">Используйте свойство **AbsolutePosition,** чтобы перейти к записи в зависимости от его расположения в объекте **Recordset** или определить ordinal положение текущей записи.</span><span class="sxs-lookup"><span data-stu-id="70904-113">Use the **AbsolutePosition** property to move to a record based on its ordinal position in the **Recordset** object, or to determine the ordinal position of the current record.</span></span> <span data-ttu-id="70904-114">Поставщик должен поддерживать соответствующие функции, чтобы это свойство было доступно.</span><span class="sxs-lookup"><span data-stu-id="70904-114">The provider must support the appropriate functionality for this property to be available.</span></span>

<span data-ttu-id="70904-115">Как и [свойство AbsolutePage,](absolutepage-property-ado.md) **AbsolutePosition** основан на 1 и равен 1, когда текущая запись является первой записью **в Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="70904-115">Like the [AbsolutePage](absolutepage-property-ado.md) property, **AbsolutePosition** is 1-based and equals 1 when the current record is the first record in the **Recordset**.</span></span> <span data-ttu-id="70904-116">Общее количество записей в объекте **Recordset** можно получить из свойства [RecordCount.](recordcount-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="70904-116">You can obtain the total number of records in the **Recordset** object from the [RecordCount](recordcount-property-ado.md) property.</span></span>

<span data-ttu-id="70904-117">При задании свойства **AbsolutePosition,** даже если оно записано в текущем кэше, ADO перезагружает кэш новой группой записей, начиная с указанной записи.</span><span class="sxs-lookup"><span data-stu-id="70904-117">When you set the **AbsolutePosition** property, even if it is to a record in the current cache, ADO reloads the cache with a new group of records starting with the record that you specified.</span></span> <span data-ttu-id="70904-118">Свойство [CacheSize](cachesize-property-ado.md) определяет размер этой группы.</span><span class="sxs-lookup"><span data-stu-id="70904-118">The [CacheSize](cachesize-property-ado.md) property determines the size of this group.</span></span>


> [!NOTE]
> <span data-ttu-id="70904-119">Свойство **AbsolutePosition** не следует использовать в качестве номера записи суррогата.</span><span class="sxs-lookup"><span data-stu-id="70904-119">You should not use the **AbsolutePosition** property as a surrogate record number.</span></span> <span data-ttu-id="70904-120">Положение данной записи меняется при удалении предыдущей записи.</span><span class="sxs-lookup"><span data-stu-id="70904-120">The position of a given record changes when you delete a preceding record.</span></span> <span data-ttu-id="70904-121">Кроме того, нет уверенности в том, что в случае повторного или повторного открытия объекта **Recordset** у данной записи будет одинаковый **absolutePosition.**</span><span class="sxs-lookup"><span data-stu-id="70904-121">There is also no assurance that a given record will have the same **AbsolutePosition** if the **Recordset** object is requeried or reopened.</span></span> <span data-ttu-id="70904-122">Закладки по-прежнему являются рекомендуемой возможностью сохранять и возвращаться в заданную позицию и являются единственным способом позиционирования во всех типах объектов **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="70904-122">Bookmarks are still the recommended way of retaining and returning to a given position, and are the only way of positioning across all types of **Recordset** objects.</span></span>


