        <?php while ($row = $result->fetch_assoc()): ?>
        <tr style="background-color:rgba(0, 0, 0, 0.16);">
            <td style="padding: 12px 15px; border: 5px solid lime;"><?php echo $row['id']; ?></td>
            <td style="padding: 12px 15px; border: 5px solid lime;"><?php echo $row['first_name']; ?></td>
            <td style="padding: 12px 15px; border: 5px solid lime;"><?php echo $row['last_name']; ?></td>
            <td style="padding: 12px 15px; border: 5px solid lime;"><?php echo $row['department']; ?></td>
            <td style="padding: 12px 15px; border: 5px solid lime;"><?php echo $row['salary']; ?></td>
            <td style="padding: 12px 15px; border: 5px solid lime;">
                <a href="edit_employee.php?id=<?php echo $row['id']; ?>" onclick="return confirm('Are you sure to edit this Employee?');" 
                    style="color: #ffffff; text-decoration: none; margin-right: 10px; padding: 5px 10px; border: 1px solid lime; border-radius: 5px;">Edit</a>
                <a href="delete_employee.php?id=<?php echo $row['id']; ?>" onclick="return confirm('Are you sure to delete this Employee?');" 
                    style="color: #ffffff; text-decoration: none; padding: 5px 10px; border: 1px solid lime; border-radius: 5px;">Delete</a>
            </td>
        </tr>
        <?php endwhile; ?>
