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
# <a name="creating-a-form-configuration-file"></a><span data-ttu-id="2c3f5-103">Создание файла конфигурации формы</span><span class="sxs-lookup"><span data-stu-id="2c3f5-103">Creating a Form Configuration File</span></span>

  
  
<span data-ttu-id="2c3f5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2c3f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2c3f5-105">Файл конфигурации формы содержит сведения о форме как в используемом диспетчере форм, так и в клиентских приложениях.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-105">A form configuration file provides information about a form both to the form manager being used and to client applications.</span></span> <span data-ttu-id="2c3f5-106">Файл конфигурации формы содержит обширную спецификацию для формы, включая свойства, публикуемые формой для клиентов обмена сообщениями, команды, реализованные в форме, и платформы, поддерживаемые формой.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-106">A form configuration file contains an extensive specification for a form, including the properties published by the form for use by messaging clients, the verbs implemented by the form, and the platforms supported by the form.</span></span>
  
<span data-ttu-id="2c3f5-107">Файл конфигурации формы — это файл с расширением. cfg и имеет формат, аналогичный файлу инициализации Windows.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-107">A form configuration file is a file with a .cfg extension, and has a format similar to a Windows initialization file.</span></span> <span data-ttu-id="2c3f5-108">Это обычный текстовый файл с несколькими разделами.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-108">It is a plain text file with a number of sections.</span></span> <span data-ttu-id="2c3f5-109">Каждый раздел начинается с имени раздела, заключенного в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-109">Each section begins with a section name, enclosed in square brackets.</span></span> <span data-ttu-id="2c3f5-110">Каждый раздел содержит одну или несколько строк, определяющих значения и параметры, относящиеся к этому разделу.</span><span class="sxs-lookup"><span data-stu-id="2c3f5-110">Each section contains one or more lines that define values and settings relevant to that section.</span></span> <span data-ttu-id="2c3f5-111">Значения имеют один из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="2c3f5-111">Values have one of the following types:</span></span>
  
- <span data-ttu-id="2c3f5-112">String</span><span class="sxs-lookup"><span data-stu-id="2c3f5-112">String</span></span>
    
- <span data-ttu-id="2c3f5-113">Отображаемая строка</span><span class="sxs-lookup"><span data-stu-id="2c3f5-113">Displayed string</span></span>
    
- <span data-ttu-id="2c3f5-114">Строка платформы</span><span class="sxs-lookup"><span data-stu-id="2c3f5-114">Platform string</span></span>
    
- <span data-ttu-id="2c3f5-115">Имя пути</span><span class="sxs-lookup"><span data-stu-id="2c3f5-115">Path name</span></span>
    
- <span data-ttu-id="2c3f5-116">Целое число</span><span class="sxs-lookup"><span data-stu-id="2c3f5-116">Integer</span></span>
    
- <span data-ttu-id="2c3f5-117">GUID</span><span class="sxs-lookup"><span data-stu-id="2c3f5-117">GUID</span></span>
    
<span data-ttu-id="2c3f5-118">Дополнительные сведения о разделах файла конфигурации формы приведены в разделе [Формат файлов конфигурации форм](file-format-of-form-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="2c3f5-118">For more information about the sections of a .cfg file, see [File Format of Form Configuration Files](file-format-of-form-configuration-files.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2c3f5-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2c3f5-119">See also</span></span>



[<span data-ttu-id="2c3f5-120">Разработка серверов форм MAPI</span><span class="sxs-lookup"><span data-stu-id="2c3f5-120">Developing MAPI Form Servers</span></span>](developing-mapi-form-servers.md)

