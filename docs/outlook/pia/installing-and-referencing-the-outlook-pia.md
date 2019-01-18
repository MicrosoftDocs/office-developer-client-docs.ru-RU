---
title: Установка и создание ссылок на Outlook PIA
TOCTitle: Installing and referencing the Outlook PIA
ms:assetid: b1afd047-dcbb-480f-ba74-993d7d7114cb
ms:mtpsurl: https://msdn.microsoft.com/library/office/bb646840(v=office.15)
ms:contentKeyID: 55119774
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 45584ae0a7050aa769368db518c9efcd5db9975a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718205"
---
# <a name="installing-and-referencing-the-outlook-pia"></a><span data-ttu-id="6d0eb-102">Установка и создание ссылок на Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="6d0eb-102">Installing and referencing the Outlook PIA</span></span>

<span data-ttu-id="6d0eb-103">Необходимо установить основную сборку взаимодействия с Outlook (PIA) в глобальный кэш сборок (GAC), чтобы включить информацию из PIA в управляемую надстройку Outlook.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-103">You must have the Outlook Primary Interop Assembly (PIA) installed in the Global Assembly Cache (GAC) before you can incorporate information from the PIA in an Outlook managed add-in.</span></span> <span data-ttu-id="6d0eb-104">По умолчанию PIA автоматически устанавливается при установке Office на компьютере для разработки.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-104">By default, the PIA is installed automatically when you install Office on the development computer.</span></span> <span data-ttu-id="6d0eb-105">Если нужно установить PIA отдельно, см. статью [Настройка компьютера для разработки решений Office](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span><span class="sxs-lookup"><span data-stu-id="6d0eb-105">However, if you need to install the PIA separately, see [Configure a computer to develop Office solutions](https://docs.microsoft.com/visualstudio/vsto/configuring-a-computer-to-develop-office-solutions?view=vs-2017).</span></span>


> [!NOTE] 
> <span data-ttu-id="6d0eb-106">Необходимо быть администратором на компьютере для разработки, чтобы установить Office PIA.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-106">You must be an administrator on the development computer to install the Office PIAs.</span></span>

<span data-ttu-id="6d0eb-107">Если после установки для создания управляемого проекта используется Visual Studio, можно добавить ссылку на компонент Microsoft Outlook 15.0 Object Library.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-107">After installation, if you are using Visual Studio to create the managed project, you can add a reference to the Microsoft Outlook 15.0 Object Library component.</span></span> <span data-ttu-id="6d0eb-108">Затем в пространстве имен **Microsoft.Office.Interop.Outlook** обозревателя объектов можно увидеть управляемые интерфейсы в PIA, имена которых соответствуют объектам в объектной модели Outlook.</span><span class="sxs-lookup"><span data-stu-id="6d0eb-108">Subsequently, in the object browser, under the **Microsoft.Office.Interop.Outlook** namespace, you can see managed interfaces in the PIA that have names corresponding to objects in the Outlook object model.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d0eb-109">См. также</span><span class="sxs-lookup"><span data-stu-id="6d0eb-109">See also</span></span>

- [<span data-ttu-id="6d0eb-110">Установка основных сборок взаимодействия Office</span><span class="sxs-lookup"><span data-stu-id="6d0eb-110">Install Office primary interop assemblies</span></span>](https://docs.microsoft.com/visualstudio/vsto/how-to-install-office-primary-interop-assemblies?view=vs-2017)
- [<span data-ttu-id="6d0eb-111">Архитектура Outlook PIA</span><span class="sxs-lookup"><span data-stu-id="6d0eb-111">Architecture of the Outlook PIA</span></span>](architecture-of-the-outlook-pia.md)

