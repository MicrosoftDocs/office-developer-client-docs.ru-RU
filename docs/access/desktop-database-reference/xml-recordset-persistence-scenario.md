---
title: Сценарий хранение записей XML
TOCTitle: XML Recordset Persistence Scenario
ms:assetid: 08f464da-10ba-b649-7571-766a40da2e04
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248825(v=office.15)
ms:contentKeyID: 48543107
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bbb8a3aa50027be7ce025a04d5987a45fee888f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482625"
---
# <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="ff88d-102">Сценарий хранение записей XML</span><span class="sxs-lookup"><span data-stu-id="ff88d-102">XML Recordset Persistence Scenario</span></span>


<span data-ttu-id="ff88d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff88d-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="xml-recordset-persistence-scenario"></a><span data-ttu-id="ff88d-104">Сценарий хранение записей XML</span><span class="sxs-lookup"><span data-stu-id="ff88d-104">XML Recordset Persistence Scenario</span></span>

<span data-ttu-id="ff88d-105">В данном сценарии создается приложение Active Server Pages (ASP), сохранение содержимого объекта **набора записей** непосредственно к объекту ASP **ответа** .</span><span class="sxs-lookup"><span data-stu-id="ff88d-105">In this scenario, you will create an Active Server Pages (ASP) application that saves the contents of a **Recordset** object directly to the ASP **Response** object.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ff88d-106">В этом случае необходимо, что сервер Internet Information Server 5.0 (IIS) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ff88d-106">This scenario requires that your server have Internet Information Server 5.0 (IIS) or later installed.</span></span></P>



<span data-ttu-id="ff88d-107">Возвращенный **набор записей** отображается в браузере Internet Explorer с помощью [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="ff88d-107">The returned **Recordset** is displayed in Internet Explorer using an [RDS.DataControl](datacontrol-object-rds.md).</span></span>

<span data-ttu-id="ff88d-108">Для создания этого сценария необходимы следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ff88d-108">The following steps are necessary to create this scenario:</span></span>

1.  <span data-ttu-id="ff88d-109">Настройка приложения.</span><span class="sxs-lookup"><span data-stu-id="ff88d-109">Set up the application.</span></span>

2.  <span data-ttu-id="ff88d-110">Получение данных.</span><span class="sxs-lookup"><span data-stu-id="ff88d-110">Get the data.</span></span>

3.  <span data-ttu-id="ff88d-111">Отправка данных.</span><span class="sxs-lookup"><span data-stu-id="ff88d-111">Send the data.</span></span>

4.  <span data-ttu-id="ff88d-112">Получение и отображения данных.</span><span class="sxs-lookup"><span data-stu-id="ff88d-112">Receive and display the data.</span></span>

<span data-ttu-id="ff88d-113">**Далее** [Шаг 1: настройки приложения](step-1-set-up-the-application.md)</span><span class="sxs-lookup"><span data-stu-id="ff88d-113">**Next**[Step 1: Set Up the Application](step-1-set-up-the-application.md)</span></span>

