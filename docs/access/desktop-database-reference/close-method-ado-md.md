---
title: Метод Close (ADO MD)
TOCTitle: Close method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 609069d04124146f311166e3ae56d8d6a793675b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296320"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="ad236-102">Метод Close (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ad236-102">Close method (ADO MD)</span></span>


<span data-ttu-id="ad236-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ad236-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ad236-104">Закрывает открытый ячейки.</span><span class="sxs-lookup"><span data-stu-id="ad236-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad236-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad236-105">Syntax</span></span>

<span data-ttu-id="ad236-106">*Cellset*. Закрыть</span><span class="sxs-lookup"><span data-stu-id="ad236-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="ad236-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="ad236-107">Remarks</span></span>

<span data-ttu-id="ad236-108">С помощью **метода Close** для закрытия объекта [Cellset](cellset-object-ado-md.md) будут высвобованы связанные данные, в том числе данные в любых связанных объектах [Cell,](cell-object-ado-md.md) [Axis,](axis-object-ado-md.md) [Position](position-object-ado-md.md)или [Member.](member-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="ad236-108">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects.</span></span> <span data-ttu-id="ad236-109">Закрытие **ячейки не** удаляет его из памяти; Вы можете изменить его параметры свойств и открыть его позже.</span><span class="sxs-lookup"><span data-stu-id="ad236-109">Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="ad236-110">Чтобы полностью исключить объект из памяти, установите переменную объекта **в Nothing**.</span><span class="sxs-lookup"><span data-stu-id="ad236-110">To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="ad236-111">Позже можно вызвать метод [Open,](open-method-ado-md.md) чтобы открыть **ячейки** с помощью той же или другой строки источника.</span><span class="sxs-lookup"><span data-stu-id="ad236-111">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string.</span></span> <span data-ttu-id="ad236-112">В то время как объект **Cellset** закрыт, при сборе любых свойств или вызове любых методов, ссылающихся на данные или метаданные, создает ошибку.</span><span class="sxs-lookup"><span data-stu-id="ad236-112">While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

