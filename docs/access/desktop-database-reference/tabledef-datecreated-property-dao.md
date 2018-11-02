---
title: Свойство TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be76ed7f9d358963ea58776327ddafbb66f9d367
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923142"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="3a71a-102">Свойство TableDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="3a71a-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="3a71a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a71a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3a71a-104">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3a71a-104">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3a71a-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="3a71a-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a71a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a71a-106">Syntax</span></span>

<span data-ttu-id="3a71a-107">*выражение* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="3a71a-107">*expression* .DateCreated</span></span>

<span data-ttu-id="3a71a-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="3a71a-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a71a-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="3a71a-109">Remarks</span></span>

<span data-ttu-id="3a71a-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="3a71a-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="3a71a-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="3a71a-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

