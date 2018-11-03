---
title: Свойство TableDef.LastUpdated (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81d8dfd040ef7df954b71f724ed1d2689d5d4b33
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928224"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="2ffdc-102">Свойство TableDef.LastUpdated (DAO)</span><span class="sxs-lookup"><span data-stu-id="2ffdc-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="2ffdc-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2ffdc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2ffdc-104">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="2ffdc-104">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="2ffdc-105">Только для чтения **Variant**.</span><span class="sxs-lookup"><span data-stu-id="2ffdc-105">Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ffdc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ffdc-106">Syntax</span></span>

<span data-ttu-id="2ffdc-107">*выражение* . LastUpdated</span><span class="sxs-lookup"><span data-stu-id="2ffdc-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="2ffdc-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="2ffdc-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ffdc-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="2ffdc-109">Remarks</span></span>

<span data-ttu-id="2ffdc-110">**DateCreated** и **LastUpdated** возвращают дату и время создания или последнего обновления.</span><span class="sxs-lookup"><span data-stu-id="2ffdc-110">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated.</span></span> <span data-ttu-id="2ffdc-111">В многопользовательской среде пользователи должны получить эти параметры непосредственно из файлового сервера, чтобы избежать несоответствия в DateCreated и параметры свойства LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="2ffdc-111">In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

