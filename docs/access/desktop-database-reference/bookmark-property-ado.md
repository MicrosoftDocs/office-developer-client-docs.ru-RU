---
title: Свойство Bookmark (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5052b25325007a5daca76baccf7414e0c7a43cd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889126"
---
# <a name="bookmark-property-ado"></a><span data-ttu-id="ec655-102">Свойство Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec655-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="ec655-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec655-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec655-104">Указывает закладки, который уникальным образом определяет текущую запись в объект [набора записей](recordset-object-ado.md) или задает текущей записи в объекте **набора записей** к записи, обозначенный допустимый закладка.</span><span class="sxs-lookup"><span data-stu-id="ec655-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="ec655-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="ec655-105">Settings and return values</span></span>

<span data-ttu-id="ec655-106">Задает или возвращает выражение **типа Variant** , которое оценивается как действительный закладке.</span><span class="sxs-lookup"><span data-stu-id="ec655-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec655-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="ec655-107">Remarks</span></span>

<span data-ttu-id="ec655-108">Используйте свойство **закладку** для сохранения положения текущей записи и вернуться на эту запись в любое время.</span><span class="sxs-lookup"><span data-stu-id="ec655-108">Use the **Bookmark** property to save the position of the current record and return to that record at any time.</span></span> <span data-ttu-id="ec655-109">Закладки доступны только в объекты **набора записей** , которые поддерживают функциональные возможности закладка.</span><span class="sxs-lookup"><span data-stu-id="ec655-109">Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="ec655-110">При открытии объекта **набора записей** , каждый из его записей имеет уникальный закладка.</span><span class="sxs-lookup"><span data-stu-id="ec655-110">When you open a **Recordset** object, each of its records has a unique bookmark.</span></span> <span data-ttu-id="ec655-111">Чтобы сохранить закладку для текущей записи, присвойте переменной значение свойства **Закладка** .</span><span class="sxs-lookup"><span data-stu-id="ec655-111">To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="ec655-112">Чтобы быстро вернуться на эту запись в любое время после перехода на другой записи, объекта **набора записей** **закладку** свойству присвоить значение переменной.</span><span class="sxs-lookup"><span data-stu-id="ec655-112">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="ec655-113">Пользователь не может быть можно просматривать значение закладки.</span><span class="sxs-lookup"><span data-stu-id="ec655-113">The user may not be able to view the value of the bookmark.</span></span> <span data-ttu-id="ec655-114">Кроме того, пользователи не следует ожидать закладки необходимо сравнить непосредственно — две закладки, связанные с той же записи могут иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="ec655-114">Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="ec655-115">При использовании метода [клонирования](clone-method-ado.md) для создания копии объекта **набора записей** идентичны параметры свойства **закладку** для исходной и повторяющихся **записей** объектов и их можно использовать попеременно.</span><span class="sxs-lookup"><span data-stu-id="ec655-115">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably.</span></span> <span data-ttu-id="ec655-116">Тем не менее закладок из разных объектов **набора записей** нельзя использовать попеременно, даже в том случае, если они были созданы на основе команду или источника.</span><span class="sxs-lookup"><span data-stu-id="ec655-116">However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="ec655-117">**Службы удаленных данных об использовании** При использовании в объект **набора записей** со стороны клиента, свойство **закладку** всегда доступен.</span><span class="sxs-lookup"><span data-stu-id="ec655-117">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

