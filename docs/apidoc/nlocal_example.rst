NLocal Example
==============

Here is a basic example of how to use the ``NLocal`` class from Qiskit:

.. code-block:: python

    from qiskit.circuit.library import NLocal
    from qiskit.circuit.library.standard_gates import RXGate, CXGate

    # Create an NLocal circuit with 3 qubits, RX as rotation, CX as entanglement, 2 repetitions
    nlocal = NLocal(
        num_qubits=3,
        rotation_blocks=RXGate(),
        entanglement_blocks=CXGate(),
        entanglement=[[0, 1], [1, 2]],
        reps=2,
        insert_barriers=True
    )
    print(nlocal)

This will create a variational circuit with alternating RX rotations and CX entangling gates, repeated twice, with barriers for clarity.

You can customize the rotation and entanglement blocks, the entanglement map, and the number of repetitions. For more advanced usage, see the full Qiskit documentation or the docstring in the source code.
