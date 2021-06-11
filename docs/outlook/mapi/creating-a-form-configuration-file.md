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
ms.openlocfilehash: 97ecafb2e4159c680fd23607f5ed6f8ea3156de7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425220"
---
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="299e1-103">Создание файла конфигурации формы</span><span class="sxs-lookup"><span data-stu-id="299e1-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="299e1-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="299e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="299e1-105">Файл конфигурации формы предоставляет сведения о форме как для используемого администратора форм, так и для клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="299e1-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="299e1-106">Файл конфигурации формы содержит обширную спецификацию формы, в том числе свойства, опубликованные формой для использования клиентами обмена сообщениями, глаголы, реализованные формой, и платформы, поддерживаемые формой.</span><span class="sxs-lookup"><span data-stu-id="299e1-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="299e1-107">Файл конфигурации формы — это файл с расширением .cfg и имеет формат, аналогичный Windows инициализации.</span><span class="sxs-lookup"><span data-stu-id="299e1-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="299e1-108">Это обычный текстовый файл с рядом разделов.</span><span class="sxs-lookup"><span data-stu-id="299e1-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="299e1-109">Каждый раздел начинается с имени раздела, заключенного в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="299e1-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="299e1-110">Каждый раздел содержит одну или несколько строк, определяя значения и параметры, соответствующие этому разделу.</span><span class="sxs-lookup"><span data-stu-id="299e1-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="299e1-111">Значения имеют один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="299e1-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="299e1-112">String</span><span class="sxs-lookup"><span data-stu-id="299e1-112">String</span></span>
    
- <span data-ttu-id="299e1-113">Отображаемая строка</span><span class="sxs-lookup"><span data-stu-id="299e1-113">Displayed string</span></span>
    
- <span data-ttu-id="299e1-114">Строка платформы</span><span class="sxs-lookup"><span data-stu-id="299e1-114">Platform string</span></span>
    
- <span data-ttu-id="299e1-115">Имя пути</span><span class="sxs-lookup"><span data-stu-id="299e1-115">Path name</span></span>
    
- <span data-ttu-id="299e1-116">Целое число</span><span class="sxs-lookup"><span data-stu-id="299e1-116">Integer</span></span>
    
- <span data-ttu-id="299e1-117">GUID</span><span class="sxs-lookup"><span data-stu-id="299e1-117">GUID</span></span>
    
<span data-ttu-id="299e1-118">Дополнительные сведения о разделах файла .cfg см. в [разделах File Format of Form Configuration Files.](file-format-of-form-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="299e1-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="299e1-119">См. также</span><span class="sxs-lookup"><span data-stu-id="299e1-119">See also</span></span>



[<span data-ttu-id="299e1-120">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="299e1-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

