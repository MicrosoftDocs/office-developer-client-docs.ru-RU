---
title: Создание файла конфигурации формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aaf3b33d-ad2d-4ef8-847f-1ab1eaf08706
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d8159d93aef020d7c9c1b56be4cf6256f80b8aa3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584172"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="5eb1e-103">Создание файла конфигурации формы</span><span class="sxs-lookup"><span data-stu-id="5eb1e-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="5eb1e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5eb1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5eb1e-105">Файл конфигурации формы сведения о формы в диспетчер форм используются и в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="5eb1e-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="5eb1e-106">Файл конфигурации формы содержит широкое спецификацию для формы, включая свойства, опубликованное формы для использования системой обмена сообщениями клиентов, команды, реализованный формы и платформ, поддерживаемых формы.</span><span class="sxs-lookup"><span data-stu-id="5eb1e-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="5eb1e-107">Файл конфигурации формы представляет собой файл с расширением .cfg и имеет формат, аналогичный файла инициализации Windows.</span><span class="sxs-lookup"><span data-stu-id="5eb1e-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="5eb1e-108">Это обычный текстовый файл с номером из разделов.</span><span class="sxs-lookup"><span data-stu-id="5eb1e-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="5eb1e-109">Каждый раздел начинается с именем раздела, заключенные в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="5eb1e-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="5eb1e-110">Каждый раздел содержит одну или несколько строк, которые определяют значения и параметры, относящиеся к этого раздела.</span><span class="sxs-lookup"><span data-stu-id="5eb1e-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="5eb1e-111">Значения использовать одну из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="5eb1e-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="5eb1e-112">String</span><span class="sxs-lookup"><span data-stu-id="5eb1e-112">String</span></span>
    
- <span data-ttu-id="5eb1e-113">Отображается строка</span><span class="sxs-lookup"><span data-stu-id="5eb1e-113">Displayed string</span></span>
    
- <span data-ttu-id="5eb1e-114">Строка платформы</span><span class="sxs-lookup"><span data-stu-id="5eb1e-114">Platform string</span></span>
    
- <span data-ttu-id="5eb1e-115">Имя пути</span><span class="sxs-lookup"><span data-stu-id="5eb1e-115">Path name</span></span>
    
- <span data-ttu-id="5eb1e-116">Целое число</span><span class="sxs-lookup"><span data-stu-id="5eb1e-116">Integer</span></span>
    
- <span data-ttu-id="5eb1e-117">GUID</span><span class="sxs-lookup"><span data-stu-id="5eb1e-117">GUID</span></span>
    
<span data-ttu-id="5eb1e-118">Дополнительные сведения о разделах файла .cfg см [файл формата из формы](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="5eb1e-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5eb1e-119">См. также</span><span class="sxs-lookup"><span data-stu-id="5eb1e-119">See also</span></span>



[<span data-ttu-id="5eb1e-120">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="5eb1e-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

