---
title: Сценарий сохранения набора записей XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fbf60cf8ef6099f8d16ab20f4441477fad1d32ab
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/01/2018
ms.locfileid: "25891172"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="0dc48-102">Сценарий сохранения набора записей XML</span><span class="sxs-lookup"><span data-stu-id="0dc48-102">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="0dc48-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dc48-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="0dc48-104">Сценарий сохранения набора записей XML</span><span class="sxs-lookup"><span data-stu-id="0dc48-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="0dc48-105">В данном сценарии создается приложение Active Server Pages (ASP), сохранение содержимого объекта **набора записей** непосредственно к объекту ASP **ответа** .</span><span class="sxs-lookup"><span data-stu-id="0dc48-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>

> [!NOTE]
> <span data-ttu-id="0dc48-106">В этом случае необходимо, что сервер Internet Information Server 5.0 (IIS) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="0dc48-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span>

<span data-ttu-id="0dc48-107">Возвращенный **набор записей** отображается в браузере Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="0dc48-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="0dc48-108">Для создания этого сценария необходимы следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0dc48-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="0dc48-109">Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="0dc48-109">Set up the application.</span></span>

2.  <span data-ttu-id="0dc48-110">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="0dc48-110">Get the data.</span></span>

3.  <span data-ttu-id="0dc48-111">Отправка данных.</span><span class="sxs-lookup"><span data-stu-id="0dc48-111">Send the data.</span></span>

4.  <span data-ttu-id="0dc48-112">Получение и отображения данных.</span><span class="sxs-lookup"><span data-stu-id="0dc48-112">Receive and display the data.</span></span>

### <a name="next-step"></a><span data-ttu-id="0dc48-113">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="0dc48-113">Next step</span></span>

[<span data-ttu-id="0dc48-114">Этап 1. Настройка приложения</span><span class="sxs-lookup"><span data-stu-id="0dc48-114">Step 1: Set Up the Application</span></span>](step-1-set-up-the-application.md)

