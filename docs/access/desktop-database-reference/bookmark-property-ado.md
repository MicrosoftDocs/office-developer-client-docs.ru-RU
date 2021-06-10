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
# <a name="bookmark-property-ado"></a><span data-ttu-id="92e0b-102">Свойство Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="92e0b-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="92e0b-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="92e0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="92e0b-104">Указывает закладки, которые однозначно идентифицируют текущую запись в объекте [Recordset](recordset-object-ado.md) или устанавливают текущую запись в объекте **Recordset** к записи, определенной допустимой закладкой.</span><span class="sxs-lookup"><span data-stu-id="92e0b-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="92e0b-105">Параметры и значения возврата</span><span class="sxs-lookup"><span data-stu-id="92e0b-105">Settings and return values</span></span>

<span data-ttu-id="92e0b-106">Задает или возвращает выражение **Variant,** которое оценивается в допустимую закладки.</span><span class="sxs-lookup"><span data-stu-id="92e0b-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="92e0b-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="92e0b-107">Remarks</span></span>

<span data-ttu-id="92e0b-108">Используйте свойство **Bookmark,** чтобы сохранить положение текущей записи и вернуться к этой записи в любое время.</span><span class="sxs-lookup"><span data-stu-id="92e0b-108">Use the **Bookmark** property to save the position of the current record and return to that record at any time.</span></span> <span data-ttu-id="92e0b-109">Закладки доступны только в **объектах Recordset,** поддерживаюх функции закладок.</span><span class="sxs-lookup"><span data-stu-id="92e0b-109">Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="92e0b-110">При открывлении **объекта Recordset** каждая из его записей имеет уникальную закладку.</span><span class="sxs-lookup"><span data-stu-id="92e0b-110">When you open a **Recordset** object, each of its records has a unique bookmark.</span></span> <span data-ttu-id="92e0b-111">Чтобы сохранить закладки для текущей записи, назначьте значение свойства **Bookmark** переменной.</span><span class="sxs-lookup"><span data-stu-id="92e0b-111">To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="92e0b-112">Чтобы быстро в любое время вернуться к данной записи после перехода к другой записи, задайте в объекте **Recordset** для свойства **Bookmark** значение данной переменной.</span><span class="sxs-lookup"><span data-stu-id="92e0b-112">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="92e0b-113">Возможно, пользователь не сможет просмотреть значение закладки.</span><span class="sxs-lookup"><span data-stu-id="92e0b-113">The user may not be able to view the value of the bookmark.</span></span> <span data-ttu-id="92e0b-114">Кроме того, пользователям не следует ожидать непосредственного сопоставимого уровня закладок : две закладки, которые относятся к одной записи, могут иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="92e0b-114">Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="92e0b-115">Если метод [Клона](clone-method-ado.md) создает копию объекта **Recordset,** параметры свойств "Закладки" для исходных и дублирующихся объектов **Recordset** идентичны, и их можно использовать взаимозаменяемо. </span><span class="sxs-lookup"><span data-stu-id="92e0b-115">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably.</span></span> <span data-ttu-id="92e0b-116">Однако нельзя использовать закладки из разных объектов **Recordset** взаимозаменяемо, даже если они были созданы из одного источника или команды.</span><span class="sxs-lookup"><span data-stu-id="92e0b-116">However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="92e0b-117">**Удаленное использование службы данных** Свойство **Bookmark** всегда доступно в клиентском объекте **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="92e0b-117">**Remote Data Service Usage** When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

