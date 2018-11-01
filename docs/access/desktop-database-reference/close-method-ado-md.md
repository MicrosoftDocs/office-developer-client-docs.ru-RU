---
title: Закройте метод (ADO MD)
TOCTitle: Close Method (ADO MD)
ms:assetid: 683788b0-0a96-a165-6b49-8d7036850756
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249406(v=office.15)
ms:contentKeyID: 48545382
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 28c5ff23470015c9b40c996a1eb5b60f74766da3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888792"
---
# <a name="close-method-ado-md"></a><span data-ttu-id="7fed1-102">Закройте метод (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7fed1-102">Close Method (ADO MD)</span></span>


<span data-ttu-id="7fed1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fed1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7fed1-104">Закрытие открытых ячеек.</span><span class="sxs-lookup"><span data-stu-id="7fed1-104">Closes an open cellset.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fed1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fed1-105">Syntax</span></span>

<span data-ttu-id="7fed1-106">*Набор ячеек*. Закрыть</span><span class="sxs-lookup"><span data-stu-id="7fed1-106">*Cellset*.Close</span></span>

## <a name="remarks"></a><span data-ttu-id="7fed1-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="7fed1-107">Remarks</span></span>

<span data-ttu-id="7fed1-108">С помощью метода **Закрыть** для закрытия объекта [ячеек](cellset-object-ado-md.md) выпустит связанных данных, включая данные в связанные [ячейки](cell-object-ado-md.md), [ось](axis-object-ado-md.md), [положение](position-object-ado-md.md)или [член](member-object-ado-md.md) объекты.</span><span class="sxs-lookup"><span data-stu-id="7fed1-108">Using the **Close** method to close a [Cellset](cellset-object-ado-md.md) object will release the associated data, including data in any related [Cell](cell-object-ado-md.md), [Axis](axis-object-ado-md.md), [Position](position-object-ado-md.md), or [Member](member-object-ado-md.md) objects.</span></span> <span data-ttu-id="7fed1-109">Закрытие **ячеек** не удаляется из памяти; можно изменить параметры его свойств и откройте его позже.</span><span class="sxs-lookup"><span data-stu-id="7fed1-109">Closing a **Cellset** does not remove it from memory; you can change its property settings and open it again later.</span></span> <span data-ttu-id="7fed1-110">Чтобы полностью удалить объект из памяти, задайте объектной переменной значение **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="7fed1-110">To completely eliminate an object from memory, set the object variable to **Nothing**.</span></span>

<span data-ttu-id="7fed1-111">Позднее можно вызвать метод [Open](open-method-ado-md.md) , и снова откройте **ячеек** , с помощью того же или другой источник строки.</span><span class="sxs-lookup"><span data-stu-id="7fed1-111">You can later call the [Open](open-method-ado-md.md) method to reopen the **Cellset** using the same or another source string.</span></span> <span data-ttu-id="7fed1-112">При закрытии объекта **ячеек** , извлечение всех свойств или вызов любых методов, ссылающиеся на базовой данных или метаданных приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="7fed1-112">While the **Cellset** object is closed, retrieving any properties or calling any methods that reference the underlying data or metadata generates an error.</span></span>

