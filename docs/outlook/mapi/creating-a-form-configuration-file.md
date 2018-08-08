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
ms.openlocfilehash: 9ceb7ad347e73f69eca3463ed2edc4438a45a21f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808237"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="7179f-103">Создание файла конфигурации формы</span><span class="sxs-lookup"><span data-stu-id="7179f-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="7179f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7179f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7179f-105">Файл конфигурации формы сведения о формы в диспетчер форм используются и в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="7179f-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="7179f-106">Файл конфигурации формы содержит широкое спецификацию для формы, включая свойства, опубликованное формы для использования системой обмена сообщениями клиентов, команды, реализованный формы и платформ, поддерживаемых формы.</span><span class="sxs-lookup"><span data-stu-id="7179f-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="7179f-107">Файл конфигурации формы представляет собой файл с расширением .cfg и имеет формат, аналогичный файла инициализации Windows.</span><span class="sxs-lookup"><span data-stu-id="7179f-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="7179f-108">Это обычный текстовый файл с номером из разделов.</span><span class="sxs-lookup"><span data-stu-id="7179f-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="7179f-109">Каждый раздел начинается с именем раздела, заключенные в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="7179f-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="7179f-110">Каждый раздел содержит одну или несколько строк, которые определяют значения и параметры, относящиеся к этого раздела.</span><span class="sxs-lookup"><span data-stu-id="7179f-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="7179f-111">Значения использовать одну из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="7179f-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="7179f-112">Строка</span><span class="sxs-lookup"><span data-stu-id="7179f-112">String</span></span>
    
- <span data-ttu-id="7179f-113">Отображается строка</span><span class="sxs-lookup"><span data-stu-id="7179f-113">Displayed string</span></span>
    
- <span data-ttu-id="7179f-114">Строка платформы</span><span class="sxs-lookup"><span data-stu-id="7179f-114">Platform string</span></span>
    
- <span data-ttu-id="7179f-115">Имя пути</span><span class="sxs-lookup"><span data-stu-id="7179f-115">Path name</span></span>
    
- <span data-ttu-id="7179f-116">Целое число</span><span class="sxs-lookup"><span data-stu-id="7179f-116">Integer</span></span>
    
- <span data-ttu-id="7179f-117">GUID</span><span class="sxs-lookup"><span data-stu-id="7179f-117">GUID</span></span>
    
<span data-ttu-id="7179f-118">Дополнительные сведения о разделах файла .cfg см [файл формата из формы](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="7179f-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7179f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7179f-119">See also</span></span>



[<span data-ttu-id="7179f-120">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="7179f-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

