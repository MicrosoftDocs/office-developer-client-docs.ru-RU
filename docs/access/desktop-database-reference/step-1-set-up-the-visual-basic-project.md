---
title: Этап 1. Настройка проекта Visual Basic
TOCTitle: 'Step 1: Set Up the Visual Basic Project'
ms:assetid: 1b8195c9-60c8-18a2-3fa2-ffdeed370748
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248954(v=office.15)
ms:contentKeyID: 48543544
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 31b81c762f192f8a56e56baf0c5e0ae5b6b6fadf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868653"
---
# <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="6de67-102">Этап 1. Настройка проекта Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6de67-102">Step 1: Set Up the Visual Basic Project</span></span>


<span data-ttu-id="6de67-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6de67-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="6de67-104">Этап 1. Настройка проекта Visual Basic</span><span class="sxs-lookup"><span data-stu-id="6de67-104">Step 1: Set Up the Visual Basic Project</span></span>

<span data-ttu-id="6de67-105">В этом сценарии предполагается, что у вас есть Microsoft Visual Basic 6.0 или более поздней версии, ADO 2.5 или более поздней версии и поставщик Microsoft OLE DB для публикации Интернет в системе.</span><span class="sxs-lookup"><span data-stu-id="6de67-105">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

<span data-ttu-id="6de67-106">**Чтобы создать проект ADO**</span><span class="sxs-lookup"><span data-stu-id="6de67-106">**To create an ADO project**</span></span>

1.  <span data-ttu-id="6de67-107">В Microsoft Visual Basic, создайте новый проект стандартный exe-ФАЙЛ.</span><span class="sxs-lookup"><span data-stu-id="6de67-107">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="6de67-108">В меню **проект** выберите команду **Справочные материалы**.</span><span class="sxs-lookup"><span data-stu-id="6de67-108">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="6de67-109">Выберите **«Библиотека 2.5 объекты данных ActiveX Microsoft**"и нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="6de67-109">Select **"Microsoft ActiveX Data Objects 2.5 Library**" and click **OK**.</span></span>

<span data-ttu-id="6de67-110">**Чтобы добавить элементы управления в форме**</span><span class="sxs-lookup"><span data-stu-id="6de67-110">**To insert controls on the main form**</span></span>

1.  <span data-ttu-id="6de67-111">Добавьте в форму Form1 элемент управления ListBox.</span><span class="sxs-lookup"><span data-stu-id="6de67-111">Add a ListBox control to Form1.</span></span> <span data-ttu-id="6de67-112">Установите для свойства **имя** lstMain.</span><span class="sxs-lookup"><span data-stu-id="6de67-112">Set its **Name** property to lstMain.</span></span>

2.  <span data-ttu-id="6de67-113">Добавьте другой элемент управления ListBox Form1.</span><span class="sxs-lookup"><span data-stu-id="6de67-113">Add another ListBox control to Form1.</span></span> <span data-ttu-id="6de67-114">Установите для свойства **имя** lstDetails.</span><span class="sxs-lookup"><span data-stu-id="6de67-114">Set its **Name** property to lstDetails.</span></span>

3.  <span data-ttu-id="6de67-115">Добавьте элемент управления TextBox в форму Form1.</span><span class="sxs-lookup"><span data-stu-id="6de67-115">Add a TextBox control to Form1.</span></span> <span data-ttu-id="6de67-116">Установите для свойства **имя** txtDetails.</span><span class="sxs-lookup"><span data-stu-id="6de67-116">Set its **Name** property to txtDetails.</span></span>

