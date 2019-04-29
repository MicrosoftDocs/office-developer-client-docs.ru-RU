---
title: Формат файлов конфигурации форм
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: d07d88d7b8b892a82832f91989e322ea3b32e040
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415553"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="36f09-103">Формат файлов конфигурации форм</span><span class="sxs-lookup"><span data-stu-id="36f09-103">File format of form configuration files</span></span>

<span data-ttu-id="36f09-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36f09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36f09-105">Файл конфигурации формы — это отформатированный файл, созданный разработчиками форм для определения формы.</span><span class="sxs-lookup"><span data-stu-id="36f09-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="36f09-106">Так как файлы конфигурации форм используются управляющими формами для загрузки форм, каждая форма должна быть определена с помощью файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="36f09-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="36f09-107">Файлы конфигурации формы должны иметь расширение. cfg filename.</span><span class="sxs-lookup"><span data-stu-id="36f09-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="36f09-108">Файл соответствует общему синтаксису файла инициализации Windows (INI-файла).</span><span class="sxs-lookup"><span data-stu-id="36f09-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="36f09-109">Он делится на именованные разделы, и каждый раздел содержит ряд записей и значений.</span><span class="sxs-lookup"><span data-stu-id="36f09-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="36f09-110">Значения имеют один из следующих типов: String, отображаемая строка, строка платформы, путь, целое число или глобальный уникальный идентификатор ( **GUID**).</span><span class="sxs-lookup"><span data-stu-id="36f09-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="36f09-111">Файлы конфигурации форм можно создавать с помощью любого текстового редактора или текстового процессора, поддерживающего сохранение текстовых файлов.</span><span class="sxs-lookup"><span data-stu-id="36f09-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

