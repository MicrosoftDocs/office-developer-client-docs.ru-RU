---
title: �������� OLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: febb6a5e-7c40-4f21-806e-7f827d1c37cf
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: b95b83ad7eedff577e4c36365c9e451f4b458173
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810045"
---
# <a name="ole-attachments"></a><span data-ttu-id="de25a-103">�������� OLE</span><span class="sxs-lookup"><span data-stu-id="de25a-103">OLE Attachments</span></span>

  
  
<span data-ttu-id="de25a-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="de25a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="de25a-p101">��������, ������� �������� ������� OLE, ���������� ��� ������� OLE 1 ����� ��� ����������� �������� �������������. ���� �������� ������ ������������� �������� �������� **IStorage** OLE 2, ������ ������ ���� ������������ � ����� OLE 1. ��� �������������� ����������� � ������� ������� **OleConvertIStorageToOLESTREAM**, ������� �������� ������ ���������� Win32 OLE.</span><span class="sxs-lookup"><span data-stu-id="de25a-p101">Attachments that are OLE objects are encoded as OLE 1 stream objects for backward compatibility. If the original object is really an OLE 2 **IStorage** object, then the object must be converted to an OLE 1 stream. This conversion is performed using the **OleConvertIStorageToOLESTREAM** function, which is part of the Win32 OLE libraries.</span></span> 
  

