---
title: Свойство Bookmark (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296796"
---
# <a name="bookmark-property-ado"></a><span data-ttu-id="54439-102">Свойство Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="54439-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="54439-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="54439-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="54439-104">Указывает закладку, которая уникально идентифицирует текущую запись в объекте [Recordset](recordset-object-ado.md) или задает для текущей записи в объекте **Recordset** запись, определенную допустимой закладкой.</span><span class="sxs-lookup"><span data-stu-id="54439-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="54439-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="54439-105">Settings and return values</span></span>

<span data-ttu-id="54439-106">Задает или возвращает выражение **типа Variant** , которое оценивается как допустимую закладку.</span><span class="sxs-lookup"><span data-stu-id="54439-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="54439-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="54439-107">Remarks</span></span>

<span data-ttu-id="54439-108">Используйте свойство **Bookmark** для сохранения позиции текущей записи и возврата к этой записи в любое время.</span><span class="sxs-lookup"><span data-stu-id="54439-108">Use the **Bookmark** property to save the position of the current record and return to that record at any time.</span></span> <span data-ttu-id="54439-109">Закладки доступны только в объектах **Recordset** , поддерживающих функции закладок.</span><span class="sxs-lookup"><span data-stu-id="54439-109">Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="54439-110">При открытии объекта **Recordset** каждая из его записей имеет уникальную закладку.</span><span class="sxs-lookup"><span data-stu-id="54439-110">When you open a **Recordset** object, each of its records has a unique bookmark.</span></span> <span data-ttu-id="54439-111">Чтобы сохранить закладку для текущей записи, присвойте переменной значение свойства **Bookmark** .</span><span class="sxs-lookup"><span data-stu-id="54439-111">To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="54439-112">Чтобы быстро в любое время вернуться к данной записи после перехода к другой записи, задайте в объекте **Recordset** для свойства **Bookmark** значение данной переменной.</span><span class="sxs-lookup"><span data-stu-id="54439-112">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="54439-113">Возможно, пользователь не сможет просматривать значение закладки.</span><span class="sxs-lookup"><span data-stu-id="54439-113">The user may not be able to view the value of the bookmark.</span></span> <span data-ttu-id="54439-114">Кроме того, пользователям не следует ожидать, что закладки напрямую сравнимы: две закладки, ссылающиеся на одну и ту же запись, могут иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="54439-114">Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="54439-115">При использовании метода [clone](clone-method-ado.md) для создания копии объекта **Recordset** параметры свойства **Bookmark** для исходного и дублирующихся объектов **Recordset** идентичны и их можно использовать в качестве взаимозаменяемых.</span><span class="sxs-lookup"><span data-stu-id="54439-115">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably.</span></span> <span data-ttu-id="54439-116">Однако нельзя использовать закладки из разных объектов **Recordset** , даже если они были созданы из одного и того же источника или команды.</span><span class="sxs-lookup"><span data-stu-id="54439-116">However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="54439-117">**Использование удаленной службы данных** При использовании в объекте **Recordset** на стороне клиента свойство **Bookmark** всегда доступно.</span><span class="sxs-lookup"><span data-stu-id="54439-117">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

