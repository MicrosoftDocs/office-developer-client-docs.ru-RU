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
# <a name="bookmark-property-ado"></a><span data-ttu-id="5d2f0-102">Свойство Bookmark (ADO)</span><span class="sxs-lookup"><span data-stu-id="5d2f0-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="5d2f0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d2f0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d2f0-104">Указывает закладку, которая уникальным образом идентифицирует текущую запись в объекте [Recordset](recordset-object-ado.md) или задает текущую запись в объекте **Recordset** для записи, определенной допустимой закладкой.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="5d2f0-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="5d2f0-105">Settings and return values</span></span>

<span data-ttu-id="5d2f0-106">Задает или возвращает выражение **Variant,** которое оценивается как допустимая закладка.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d2f0-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="5d2f0-107">Remarks</span></span>

<span data-ttu-id="5d2f0-108">Используйте свойство **Bookmark** для сохранения позиции текущей записи и возврата к этой записи в любое время.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-108">Use the **Bookmark** property to save the position of the current record and return to that record at any time.</span></span> <span data-ttu-id="5d2f0-109">Закладки доступны только в **объектах Recordset,** поддерживаюх функции закладок.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-109">Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="5d2f0-110">При открываемом **объекте Recordset** каждая из записей имеет уникальную закладку.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-110">When you open a **Recordset** object, each of its records has a unique bookmark.</span></span> <span data-ttu-id="5d2f0-111">Чтобы сохранить закладку для текущей записи, назначьте значение свойства **Bookmark** переменной.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-111">To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable.</span></span> <span data-ttu-id="5d2f0-112">Чтобы быстро в любое время вернуться к данной записи после перехода к другой записи, задайте в объекте **Recordset** для свойства **Bookmark** значение данной переменной.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-112">To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="5d2f0-113">Возможно, пользователь не сможет просмотреть значение закладки.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-113">The user may not be able to view the value of the bookmark.</span></span> <span data-ttu-id="5d2f0-114">Кроме того, пользователи не должны ожидать, что закладки будут напрямую сравнимы — две закладки, которые ссылаются на ту же запись, могут иметь разные значения.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-114">Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="5d2f0-115">Если вы используете метод [Clone](clone-method-ado.md) для создания копии объекта **Recordset,** параметры свойства **Bookmark** для исходного и дубликатов объектов **Recordset** идентичны, и их можно использовать взаимозаменяемо.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-115">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably.</span></span> <span data-ttu-id="5d2f0-116">Однако нельзя использовать закладки из разных объектов **Recordset** взаимозаменяемо, даже если они были созданы из одного источника или команды.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-116">However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="5d2f0-117">**Использование удаленной службы данных** При клиентском объекте **Recordset** свойство **Bookmark** всегда доступно.</span><span class="sxs-lookup"><span data-stu-id="5d2f0-117">**Remote Data Service Usage** When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

