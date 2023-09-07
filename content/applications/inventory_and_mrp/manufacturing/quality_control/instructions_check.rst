==========================
Instructions quality check
==========================

.. |QCP| replace:: :abbr:`QCP (Quality Control Point)`

In Odoo *Quality*, an *Instructions* check is one of the quality check types that can be selected
when creating a new quality check or :ref:`Quality Control Point
<manufacturing/quality_control/quality-control-points>` (QCP). Instructions checks consist of a text
entry field that allows the creator to provide instructions for how to complete the check.

There are two distinct ways that Instructions quality checks can be created. A single check can be
manually created. Alternatively, a |QCP| can be configured that will automatically create checks at
a predetermined interval.

This documentation will only detail the configuration options and processing steps that are unique
to Instructions quality checks. For a full overview of all the configuration options available when
creating a single check or a |QCP|, see the documentation on :ref:`Quality checks
<manufacturing/quality_control/quality-checks>` and :ref:`Quality Control Points
<manufacturing/quality_control/quality-control-points>`.

Create an Instructions quality check
====================================

Instructions quality checks can be created by navigating to :menuselection:`Quality --> Quality
Control --> Quality Checks`, and clicking :guilabel:`New`. It is also possible to create a |QCP|
that is configured to automatically create an Instructions quality check when certain criteria is
met. To do so, navigate to :menuselection:`Quality --> Quality Control --> Control Points`, and
click :guilabel:`New`.

On the quality check or |QCP| form, select :guilabel:`Instructions` from the :guilabel:`Type`
drop-down field. When creating a single quality check, enter the instructions for how to complete
the check in the :guilabel:`Instructions` text field of the :guilabel:`Notes` tab at the bottom of
the form. When creating a |QCP|, enter the instructions for how to complete the checks it creates in
the text field of the :guilabel:`Instructions` tab at the bottom of the form.

Fill out the remaining required fields for the quality check or |QCP|, as detailed in the
documentation for :ref:`Quality checks <manufacturing/quality_control/quality-checks>` and
:ref:`Quality Control Points <manufacturing/quality_control/quality-control-points>`. Finally, click
:guilabel:`Save` to create the quality check or |QCP|.

Process an Instructions quality check
=====================================

To process an Instructions quality check, select a manufacturing order or inventory order (receipt,
delivery, return, etc.). Manufacturing orders can be selected by navigating to
:menuselection:`Manufacturing --> Operations --> Manufacturing Orders`, and clicking on an order.
Inventory orders can be selected by navigating to :menuselection:`Inventory`, clicking the:guilabel:`# To Process` button on an operation card, and selecting an order.

On the selected manufacturing or inventory order, a purple :guilabel:`Quality Checks` button appears
at the top of the order if the order has quality checks that need to be completed. Click the button
to open the :guilabel:`Quality Check` pop-up window, which shows all of the quality checks required
for that order.

.. image:: instructions_check/quality-check-pop-up.png
   :align: center
   :alt: The Quality Check pop-up window on a manufacturing or inventory order.

To complete an Instructions quality check, follow the instructions detailed in the
:guilabel:`Quality Check` pop-up window. Finally, click :guilabel:`Validate` to confirm that the
check has been completed.

If an issue is discovered during the quality check, a quality alert may need to be created. To do
so, click the :guilabel:`Quality Alert` button at the top of the manufacturing or inventory.
Clicking :guilabel:`Quality Alert` opens a quality alert form on a new page. For a complete guide on
how to fill out the quality alert form, view the documentation on :ref:`Quality alerts
<manufacturing/quality_control/quality-alerts>`.

Process a work order Instructions quality check
===============================================

When configuring a |QCP| that is triggered during manufacturing, a specific work order can also be
specified in the :guilabel:`Work Order Operation` field on the |QCP| form. If a work order is
specified, an Instructions quality check is created for that specific work order, rather than the
manufacturing order as a whole.

Quality checks configured for work orders must be completed from the tablet view. To do so, begin by
navigating to :menuselection:`Manufacturing --> Operations --> Manufacturing Orders`. Select a
manufacturing order that includes a work order for which a quality check is required. Open the
tablet view for that work order by clicking the :guilabel:`📱 (tablet)` tablet view button on the
order's line.

With tablet view open, complete the steps listed on the left side of the screen until the
Instructions quality check step is reached. Upon reaching the check, the instructions for how to
complete it will appear at the top of the screen. Follow the instructions, then click
:guilabel:`Next` to move on to the next step.

.. image:: instructions_check/work-order-instructions-check.png
   :align: center
   :alt: An instructions check for a work order.

If an issue is discovered during the quality check, a quality alert may need to be created. To do
so, click the :guilabel:`☰ (menu)` tablet view menu button, and select :guilabel:`Quality Alert`
from the :guilabel:`Menu` pop-up window. A :guilabel:`Quality Alerts` pop-up window appears, from
which a quality alert can be created. For a complete guide to quality alert creation, view the
documentation on :ref:`Quality alerts <manufacturing/quality_control/quality-alerts>`.

.. image:: instructions_check/work-order-menu.png
   :align: center
   :alt: The Quality Alert button on the work order menu.
